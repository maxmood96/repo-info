<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `docker`

-	[`docker:27`](#docker27)
-	[`docker:27-cli`](#docker27-cli)
-	[`docker:27-dind`](#docker27-dind)
-	[`docker:27-dind-rootless`](#docker27-dind-rootless)
-	[`docker:27-windowsservercore`](#docker27-windowsservercore)
-	[`docker:27-windowsservercore-1809`](#docker27-windowsservercore-1809)
-	[`docker:27-windowsservercore-ltsc2022`](#docker27-windowsservercore-ltsc2022)
-	[`docker:27.3`](#docker273)
-	[`docker:27.3-cli`](#docker273-cli)
-	[`docker:27.3-dind`](#docker273-dind)
-	[`docker:27.3-dind-rootless`](#docker273-dind-rootless)
-	[`docker:27.3-windowsservercore`](#docker273-windowsservercore)
-	[`docker:27.3-windowsservercore-1809`](#docker273-windowsservercore-1809)
-	[`docker:27.3-windowsservercore-ltsc2022`](#docker273-windowsservercore-ltsc2022)
-	[`docker:27.3.0`](#docker2730)
-	[`docker:27.3.0-alpine3.20`](#docker2730-alpine320)
-	[`docker:27.3.0-cli`](#docker2730-cli)
-	[`docker:27.3.0-cli-alpine3.20`](#docker2730-cli-alpine320)
-	[`docker:27.3.0-dind`](#docker2730-dind)
-	[`docker:27.3.0-dind-alpine3.20`](#docker2730-dind-alpine320)
-	[`docker:27.3.0-dind-rootless`](#docker2730-dind-rootless)
-	[`docker:27.3.0-windowsservercore`](#docker2730-windowsservercore)
-	[`docker:27.3.0-windowsservercore-1809`](#docker2730-windowsservercore-1809)
-	[`docker:27.3.0-windowsservercore-ltsc2022`](#docker2730-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:e2c2ce1047f733140c5482803421c0546ff1348976d149eb410a57671ee12830
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

### `docker:27-cli` - linux; amd64

```console
$ docker pull docker@sha256:d3f53f04a54f267d3ef5b1539acb571e18edbd93c59cd607c78481f09f256bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67538322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9b9b7816c276026ce893fe521cead2138a79d9fd77dcd6c88ef7ee83dca3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7144b3a77df68d38e8f325d5ab14d8eb9f3c7b6487920fd47e0629e9436964c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bdaed9a9aa271db1c445274012e2bf42a1800521fe3170d10526b66034839`

```dockerfile
```

-	Layers:
	-	`sha256:72073a9eff31ba096fe1fae94caece9532f497fb7e7c1c29103428ea4680b9b9`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27-dind` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:860cab1cc94b17ff8bc6e2ec1c0882fa179bb06e965b234cfeeca01ba34cef34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:011f44ad292449b005e13f452dbaf255ac6313bb6fcb457006bfa02735a879a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154375757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf40999a78c9447755ea43f7ecda21896bfdabc78123c16862601632ab15480`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833b58e1c9f721970be98de60780ebe18f30d978afba5d2b87009eb9da04eb1`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 981.0 KB (980974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9727375ad4ca2351dc1a7ddf3bed1e1d19ea4996ed219a06ae1ba567211fa57`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8de45c8663ae2fa91ba9d08ff75c873db2542d752584abad65248d4843a842`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb73db4a39692c249a35b7b5219bfd496b303943e55dec42443bad09414ada`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 21.3 MB (21303255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ba09f0b98ab05f46c8fede63bc1a5601eae712c663d461eb4e71ad12f4f80`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d512af7333a03b27ac711569309c50c9bd3c7fb3b11f0f126b035d24c1c12f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0d65edc0577804ea7800457813e236234e905030d55fadd001057a5d38123`

```dockerfile
```

-	Layers:
	-	`sha256:ec415bd8ff09625b5079a44a9bdc9a6884247f9406795291abc958fd1ebc7884`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 30.6 KB (30579 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea59cfc4286369dd63f9f02b55a0b10da2e5fd82b32d28edfacecbcc03f23685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148544618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129957c24f7ff56f223ca33540a9ab2f1f9de85a1cee85e222dd36997505bff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cec37f898c9f6f9909d7b634883fd20d8a92f53ea5501bd94705eeff5d0bb9`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 1.0 MB (1023141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e878cfe040e35d3dc9e1c799d55d024f45e5100653a98e5c1888cd5e1d1d425`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b4d74576a831213366ad9645aa5a3c9c3ad5100b109eb2bd424d106e7d29e`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baefe49aa29471449d9b643ee076a928ec293fac19990e34e8f60da668f2a9a`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 23.2 MB (23155435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85c24903682cbd51034663d17eaee266c0c0ddd85e8a2db679c465fcca598e`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:083f025c1d81cb1bab37f7bcee4a9a3cab095f651828ff4fad4f52149f80d8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2936fef0cebf7e0f5070dce2c3efcb446cabb6b9b1f2be9eb5cc3c2ad0a8ce65`

```dockerfile
```

-	Layers:
	-	`sha256:0b04156c25e924a7cae508508be283f3d84294415bbec341cb4dc3a0f4d72ef7`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:2d3e908e028f64af2dc40f03d99afbf47bac68ba78ca11ab817a8fb1aec495f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:2cd33cc5181c44eddcacfa9db5d530579e7766b8574349fdd0fc204ca8009fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d436ba51852b1b7153307c438211d920860c7c1f8afe56ff64e0c89ec8eb79c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-cli`

```console
$ docker pull docker@sha256:e2c2ce1047f733140c5482803421c0546ff1348976d149eb410a57671ee12830
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

### `docker:27.3-cli` - linux; amd64

```console
$ docker pull docker@sha256:d3f53f04a54f267d3ef5b1539acb571e18edbd93c59cd607c78481f09f256bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67538322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9b9b7816c276026ce893fe521cead2138a79d9fd77dcd6c88ef7ee83dca3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7144b3a77df68d38e8f325d5ab14d8eb9f3c7b6487920fd47e0629e9436964c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bdaed9a9aa271db1c445274012e2bf42a1800521fe3170d10526b66034839`

```dockerfile
```

-	Layers:
	-	`sha256:72073a9eff31ba096fe1fae94caece9532f497fb7e7c1c29103428ea4680b9b9`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3-dind` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind-rootless`

```console
$ docker pull docker@sha256:860cab1cc94b17ff8bc6e2ec1c0882fa179bb06e965b234cfeeca01ba34cef34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:011f44ad292449b005e13f452dbaf255ac6313bb6fcb457006bfa02735a879a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154375757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf40999a78c9447755ea43f7ecda21896bfdabc78123c16862601632ab15480`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833b58e1c9f721970be98de60780ebe18f30d978afba5d2b87009eb9da04eb1`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 981.0 KB (980974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9727375ad4ca2351dc1a7ddf3bed1e1d19ea4996ed219a06ae1ba567211fa57`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8de45c8663ae2fa91ba9d08ff75c873db2542d752584abad65248d4843a842`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb73db4a39692c249a35b7b5219bfd496b303943e55dec42443bad09414ada`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 21.3 MB (21303255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ba09f0b98ab05f46c8fede63bc1a5601eae712c663d461eb4e71ad12f4f80`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d512af7333a03b27ac711569309c50c9bd3c7fb3b11f0f126b035d24c1c12f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0d65edc0577804ea7800457813e236234e905030d55fadd001057a5d38123`

```dockerfile
```

-	Layers:
	-	`sha256:ec415bd8ff09625b5079a44a9bdc9a6884247f9406795291abc958fd1ebc7884`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 30.6 KB (30579 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea59cfc4286369dd63f9f02b55a0b10da2e5fd82b32d28edfacecbcc03f23685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148544618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129957c24f7ff56f223ca33540a9ab2f1f9de85a1cee85e222dd36997505bff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cec37f898c9f6f9909d7b634883fd20d8a92f53ea5501bd94705eeff5d0bb9`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 1.0 MB (1023141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e878cfe040e35d3dc9e1c799d55d024f45e5100653a98e5c1888cd5e1d1d425`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b4d74576a831213366ad9645aa5a3c9c3ad5100b109eb2bd424d106e7d29e`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baefe49aa29471449d9b643ee076a928ec293fac19990e34e8f60da668f2a9a`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 23.2 MB (23155435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85c24903682cbd51034663d17eaee266c0c0ddd85e8a2db679c465fcca598e`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:083f025c1d81cb1bab37f7bcee4a9a3cab095f651828ff4fad4f52149f80d8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2936fef0cebf7e0f5070dce2c3efcb446cabb6b9b1f2be9eb5cc3c2ad0a8ce65`

```dockerfile
```

-	Layers:
	-	`sha256:0b04156c25e924a7cae508508be283f3d84294415bbec341cb4dc3a0f4d72ef7`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-windowsservercore`

```console
$ docker pull docker@sha256:2d3e908e028f64af2dc40f03d99afbf47bac68ba78ca11ab817a8fb1aec495f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27.3-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-1809`

```console
$ docker pull docker@sha256:2cd33cc5181c44eddcacfa9db5d530579e7766b8574349fdd0fc204ca8009fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27.3-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d436ba51852b1b7153307c438211d920860c7c1f8afe56ff64e0c89ec8eb79c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27.3-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.0`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3.0` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-alpine3.20`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3.0-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-cli`

```console
$ docker pull docker@sha256:e2c2ce1047f733140c5482803421c0546ff1348976d149eb410a57671ee12830
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

### `docker:27.3.0-cli` - linux; amd64

```console
$ docker pull docker@sha256:d3f53f04a54f267d3ef5b1539acb571e18edbd93c59cd607c78481f09f256bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67538322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9b9b7816c276026ce893fe521cead2138a79d9fd77dcd6c88ef7ee83dca3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:7144b3a77df68d38e8f325d5ab14d8eb9f3c7b6487920fd47e0629e9436964c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bdaed9a9aa271db1c445274012e2bf42a1800521fe3170d10526b66034839`

```dockerfile
```

-	Layers:
	-	`sha256:72073a9eff31ba096fe1fae94caece9532f497fb7e7c1c29103428ea4680b9b9`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-cli-alpine3.20`

```console
$ docker pull docker@sha256:e2c2ce1047f733140c5482803421c0546ff1348976d149eb410a57671ee12830
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

### `docker:27.3.0-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:d3f53f04a54f267d3ef5b1539acb571e18edbd93c59cd607c78481f09f256bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67538322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9b9b7816c276026ce893fe521cead2138a79d9fd77dcd6c88ef7ee83dca3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:7144b3a77df68d38e8f325d5ab14d8eb9f3c7b6487920fd47e0629e9436964c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bdaed9a9aa271db1c445274012e2bf42a1800521fe3170d10526b66034839`

```dockerfile
```

-	Layers:
	-	`sha256:72073a9eff31ba096fe1fae94caece9532f497fb7e7c1c29103428ea4680b9b9`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-dind`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3.0-dind` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-dind-alpine3.20`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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

### `docker:27.3.0-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-dind-rootless`

```console
$ docker pull docker@sha256:860cab1cc94b17ff8bc6e2ec1c0882fa179bb06e965b234cfeeca01ba34cef34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3.0-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:011f44ad292449b005e13f452dbaf255ac6313bb6fcb457006bfa02735a879a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154375757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf40999a78c9447755ea43f7ecda21896bfdabc78123c16862601632ab15480`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833b58e1c9f721970be98de60780ebe18f30d978afba5d2b87009eb9da04eb1`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 981.0 KB (980974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9727375ad4ca2351dc1a7ddf3bed1e1d19ea4996ed219a06ae1ba567211fa57`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8de45c8663ae2fa91ba9d08ff75c873db2542d752584abad65248d4843a842`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb73db4a39692c249a35b7b5219bfd496b303943e55dec42443bad09414ada`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 21.3 MB (21303255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ba09f0b98ab05f46c8fede63bc1a5601eae712c663d461eb4e71ad12f4f80`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d512af7333a03b27ac711569309c50c9bd3c7fb3b11f0f126b035d24c1c12f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0d65edc0577804ea7800457813e236234e905030d55fadd001057a5d38123`

```dockerfile
```

-	Layers:
	-	`sha256:ec415bd8ff09625b5079a44a9bdc9a6884247f9406795291abc958fd1ebc7884`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 30.6 KB (30579 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.0-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea59cfc4286369dd63f9f02b55a0b10da2e5fd82b32d28edfacecbcc03f23685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148544618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129957c24f7ff56f223ca33540a9ab2f1f9de85a1cee85e222dd36997505bff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cec37f898c9f6f9909d7b634883fd20d8a92f53ea5501bd94705eeff5d0bb9`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 1.0 MB (1023141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e878cfe040e35d3dc9e1c799d55d024f45e5100653a98e5c1888cd5e1d1d425`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b4d74576a831213366ad9645aa5a3c9c3ad5100b109eb2bd424d106e7d29e`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baefe49aa29471449d9b643ee076a928ec293fac19990e34e8f60da668f2a9a`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 23.2 MB (23155435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85c24903682cbd51034663d17eaee266c0c0ddd85e8a2db679c465fcca598e`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.0-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:083f025c1d81cb1bab37f7bcee4a9a3cab095f651828ff4fad4f52149f80d8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2936fef0cebf7e0f5070dce2c3efcb446cabb6b9b1f2be9eb5cc3c2ad0a8ce65`

```dockerfile
```

-	Layers:
	-	`sha256:0b04156c25e924a7cae508508be283f3d84294415bbec341cb4dc3a0f4d72ef7`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.0-windowsservercore`

```console
$ docker pull docker@sha256:2d3e908e028f64af2dc40f03d99afbf47bac68ba78ca11ab817a8fb1aec495f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27.3.0-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3.0-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.0-windowsservercore-1809`

```console
$ docker pull docker@sha256:2cd33cc5181c44eddcacfa9db5d530579e7766b8574349fdd0fc204ca8009fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27.3.0-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.0-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d436ba51852b1b7153307c438211d920860c7c1f8afe56ff64e0c89ec8eb79c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27.3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:e2c2ce1047f733140c5482803421c0546ff1348976d149eb410a57671ee12830
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
$ docker pull docker@sha256:d3f53f04a54f267d3ef5b1539acb571e18edbd93c59cd607c78481f09f256bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67538322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c9b9b7816c276026ce893fe521cead2138a79d9fd77dcd6c88ef7ee83dca3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:7144b3a77df68d38e8f325d5ab14d8eb9f3c7b6487920fd47e0629e9436964c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c76bdaed9a9aa271db1c445274012e2bf42a1800521fe3170d10526b66034839`

```dockerfile
```

-	Layers:
	-	`sha256:72073a9eff31ba096fe1fae94caece9532f497fb7e7c1c29103428ea4680b9b9`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37f27c773213521f3b9f50b1bea66893bff8cfdeb6b32ef4c0e848a030a187e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62807970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba098cb71ad32dd006eb0a19187914173eb33de03b198b5fde798eed92a6bc58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:8d75f23a7f71e324101f62e4910ebcd382df1e5b1de7c681a6e4cb6cdb51239f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d022f57c2745434cdb5a16d53bf882cfff444c2dfa89bae5a7ed046edeff0c`

```dockerfile
```

-	Layers:
	-	`sha256:230a88f840c3aac47eed4236aa13bb6a08174da6a6206d828702c6e3e539e66b`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 38.1 KB (38070 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:92cd3b7461e08430c9c8b0ed5d4901e0488e284933a85054fda8f8f8023c7f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c204650295cc9e25dec97762b7a1e329f9096943adb717615dd050b04da93e17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:d05c59320fc8170b965528a28318d76cc3f86132d619ad1abef819b8874a14eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78e41f7a9e5cff872b1477eb6418d9b44458efb85786cae50dc1b0c591c6eb`

```dockerfile
```

-	Layers:
	-	`sha256:1c05414271ca6215055155152eac69a122f18be18f74b0bb6ca2501c28e886e5`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 38.1 KB (38071 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:86b728ef94ed08000296013516632982f9045b3a267320f45f788a1d87837222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63797168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ebacfdc77c1349a11d7396eb11de6e948d8520bb119e3b6d013965e73739e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:64b5880805081e227f6d4a927b96888d67d4a31c3f9b4b8b266dff874ed5476e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9bcf782079c0ad78e0609c8b6af69b3ed5cef3331845bbf72ad615cb3eb46f`

```dockerfile
```

-	Layers:
	-	`sha256:06b348c580d845a356c7f2c8bb62a6c60ea047e84244306dd8cf0189fe150536`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 38.2 KB (38225 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:860cab1cc94b17ff8bc6e2ec1c0882fa179bb06e965b234cfeeca01ba34cef34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:011f44ad292449b005e13f452dbaf255ac6313bb6fcb457006bfa02735a879a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154375757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf40999a78c9447755ea43f7ecda21896bfdabc78123c16862601632ab15480`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a833b58e1c9f721970be98de60780ebe18f30d978afba5d2b87009eb9da04eb1`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 981.0 KB (980974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9727375ad4ca2351dc1a7ddf3bed1e1d19ea4996ed219a06ae1ba567211fa57`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8de45c8663ae2fa91ba9d08ff75c873db2542d752584abad65248d4843a842`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcb73db4a39692c249a35b7b5219bfd496b303943e55dec42443bad09414ada`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 21.3 MB (21303255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4ba09f0b98ab05f46c8fede63bc1a5601eae712c663d461eb4e71ad12f4f80`  
		Last Modified: Thu, 19 Sep 2024 23:49:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d512af7333a03b27ac711569309c50c9bd3c7fb3b11f0f126b035d24c1c12f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0d65edc0577804ea7800457813e236234e905030d55fadd001057a5d38123`

```dockerfile
```

-	Layers:
	-	`sha256:ec415bd8ff09625b5079a44a9bdc9a6884247f9406795291abc958fd1ebc7884`  
		Last Modified: Thu, 19 Sep 2024 23:49:12 GMT  
		Size: 30.6 KB (30579 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ea59cfc4286369dd63f9f02b55a0b10da2e5fd82b32d28edfacecbcc03f23685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148544618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129957c24f7ff56f223ca33540a9ab2f1f9de85a1cee85e222dd36997505bff`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cec37f898c9f6f9909d7b634883fd20d8a92f53ea5501bd94705eeff5d0bb9`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 1.0 MB (1023141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e878cfe040e35d3dc9e1c799d55d024f45e5100653a98e5c1888cd5e1d1d425`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b4d74576a831213366ad9645aa5a3c9c3ad5100b109eb2bd424d106e7d29e`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baefe49aa29471449d9b643ee076a928ec293fac19990e34e8f60da668f2a9a`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 23.2 MB (23155435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff85c24903682cbd51034663d17eaee266c0c0ddd85e8a2db679c465fcca598e`  
		Last Modified: Thu, 19 Sep 2024 23:49:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:083f025c1d81cb1bab37f7bcee4a9a3cab095f651828ff4fad4f52149f80d8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2936fef0cebf7e0f5070dce2c3efcb446cabb6b9b1f2be9eb5cc3c2ad0a8ce65`

```dockerfile
```

-	Layers:
	-	`sha256:0b04156c25e924a7cae508508be283f3d84294415bbec341cb4dc3a0f4d72ef7`  
		Last Modified: Thu, 19 Sep 2024 23:48:59 GMT  
		Size: 31.0 KB (31006 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:e16df3c5e703eae2b2162358f33af9db78c2a9c1721b496fababceec26859742
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
$ docker pull docker@sha256:4f92df6bf3f21af1e11339debbc28bfa5e0fa43e2d7e1f513e010b46c80717b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132090173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf518b0191fd756303180092be98f66a42a5ac5bdc6ea057daf035795f111488`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298992de1962a0432cd7aec609d0caa30b6b06752ef5ade05c35d7ef8f6ea05e`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 7.9 MB (7872597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd0c8c4b9afb5de0f42fbb643e7c913a138772ade3eae593f28a015492718d`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13ee56af6335ba6cedb9b634871b3b3f9a72e84f40edc59b359b4f3796720d8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.6 MB (18563578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fba0863be023fe8bd1e1832d2d58bb055211cb5040cd72fb8aaca37054ed4e8`  
		Last Modified: Thu, 19 Sep 2024 21:58:45 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22949749695dd623ba6cb083f62843bf9685c5d946c81e3ecc6e32f3a97d226c`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 19.0 MB (19038468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f79b8433c994d6de2ce37bb1b39c3b649e6f43e119cee053994187d06bb81`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d364f2f56bf3c1f7f1d10312a21c201788bffe5049fbbc95eda71677a673530`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba865f594754dfac42dc8365a4303a0ed6067eedbd08d559e44c403f452ef34b`  
		Last Modified: Thu, 19 Sep 2024 21:58:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942cc5b2c59bacd40b6c9b67490178f535aaf41ab34933f341cd02e23efbe30`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 6.7 MB (6657930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2229e8a847bbe7d46cee82145325a5e23ed11c65b643ef59e0ca330452096560`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 89.2 KB (89216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a7bb3e4da6ee33c63d8bf60e9f8271a1c58636b4f91867032aefd9d8d80734`  
		Last Modified: Thu, 19 Sep 2024 22:49:35 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe6df610590dbc5b879f19ed86628fb031ec49c414cadbe7dad7e82e7e6ada9`  
		Last Modified: Thu, 19 Sep 2024 22:49:37 GMT  
		Size: 57.8 MB (57798912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c961f8c7de850e273d6782577b64e9aab64990532a7cfa3d30714541d2e5939d`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9733f05320cf784c1080c61c5daa36a6d2657580af7c7ef7ef1e7721910191`  
		Last Modified: Thu, 19 Sep 2024 22:49:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:cb01460e8ee606948fb1f16e11802d14beb74b3edb94aa96f5c8f6aac9d4939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a863dea6574016157ed4e0ea8a1936c979a28de6e50e2d214a92ed896cecfc2`

```dockerfile
```

-	Layers:
	-	`sha256:a9900541fd1d0dccdeac17047551b3b61feda40072756263c051716cad7f0bd0`  
		Last Modified: Thu, 19 Sep 2024 22:49:34 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:b9a13c0fc2828d59796398d48b5b1c264fe770994ebec2a8c8a2a5b6324227fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bf6844ac70c11dd4d047564852c350f7109bc2aaecfcb05addd42ac9e084ed`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1eee09bdc12fa3ccb80788ee946d0dd519809f632c19f750cef5b4162398d`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 7.8 MB (7807744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98caf3bd1b61416ca414dbe14aa026849a7c16b67dd0ccf0788356d5b79cd8df`  
		Last Modified: Sat, 07 Sep 2024 02:16:26 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0b141bbd0491e967144a969f4a5dd3f181572b45a35846c163b2f7fb16fff`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 16.6 MB (16602008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c424c0c6a0742c0277dc308d0fe359e510aaed8376709939f0a8638ca53db4`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.1 MB (17145024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfc493cfb16e6ad03efdc9b75046bfff7cce80b344d35f396b97b30318cf416`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 17.9 MB (17884524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61dd2e956222db247b7ae204b7aaa46d3258e1dc4a3a8eb5499cb8869fbc86`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f775b54f05783d1f92671629aa6ca77c73e9614ae441607b1ca84f90866661bd`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788a88f1bf3a5512e6c446a3342d44c62533fe8b5a915effd2c20805904f82fb`  
		Last Modified: Thu, 19 Sep 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70790ed885a27e4eccbc56fe05df97cdfc968aa4647c2582f4413854da09866`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 7.0 MB (6984298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fd2634c40e3c9cf1f89e40f99099501c1e3835cad14b18552c5e6952046be`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 88.4 KB (88396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3516c064229131a39e04071e95d5c48dfabf6aa0258d061e2b97515fdf822`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5915de899f7c411b170c466a5a756e2a4a7f54d59a0b540cf81ede8e427ee71`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944a9cd6fa3d4addc5b56bec3578a3189cc3e846ff1de56a64303267f45b3c00`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293c9ef2d8f777f7ce13b25285a68f748b943e68de0dcc0713976df037ecf0b`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:3d097ae596840a1dd99311288fdf73bcfd8afa8676af7214ad510bd5dc262345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e17aee95a1f7724aaffbf6938c7b1e563b34637a9c067338646c323f4e88a`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5522470ef2d3c3edd5f02d92c4b227b7552d0b5ed19249455bbc6aa72d065`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34733 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:dadb55484e3e3a6a49958829d5d6816f480bf9b669fc35dd306cd3c448ede757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121751449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9dddceb42be0898c7015e8a6fd0277a8fd033bf2b04cd08c3b033d6a3f8e80`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aecd18e96db0e798cea3a61d4609cb72114897d702c2cc4d94b343f2022c1a`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 7.1 MB (7143851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296e44b1219069fd8f13cf994371b92a27c2aa5540babbd15cfa3dc868e0ad8e`  
		Last Modified: Sat, 07 Sep 2024 02:22:27 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db804da1346bf4bb2c942a2171e09d9e213b93b257e894853557c330588e585a`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 16.6 MB (16593866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a34d024b61cc94ff4f843011cbf3ae8c529135055ddd8f8c523f931e8355c2`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.1 MB (17135231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9af1c212f31da6ad713bae019fc735dcec18dbb707d83cb685ae4a5a39cf03`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 17.9 MB (17871275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124f0144a5ccd59b81b58b00adbe1b456cb061549ec3c9c3259e4106c7ff8cb8`  
		Last Modified: Thu, 19 Sep 2024 21:58:35 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc40ca55334e981eb62c46750b14d4415da578dc79a6bd4368bbd8296c54a13e`  
		Last Modified: Thu, 19 Sep 2024 21:58:36 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb877b2e39ba8ceaf28b46bbf1d99886c19ea1229bac3caa7dfc17a0fc9156bc`  
		Last Modified: Thu, 19 Sep 2024 21:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450502e9478410ef6b7a783cae64f7677db8f2c04ba1630c4d9d8769abe5bb26`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 6.3 MB (6308136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0032cf9fe70ca917791b5fb83fbef5c9116100c5ae45dceee51b43d45164186`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 84.5 KB (84483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035e0781b06e88d478acba62bd731af2ff8bc7364c18b41067a7d27d96a3122`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0415f8ff065bc6a911ef66ee34796c1ab53ae0e828606507e32055a0ae2d38`  
		Last Modified: Thu, 19 Sep 2024 22:49:24 GMT  
		Size: 53.5 MB (53511141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132f69afc848b29ccff7080f09f7316fb68e04d1c65a73ef78c30438f6f4f1b0`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2671671235c422e5914ca6337b058ac63fd557b3e283347a6bb92ff6e793f1a1`  
		Last Modified: Thu, 19 Sep 2024 22:49:23 GMT  
		Size: 3.3 KB (3263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a06db519acb489c12a5a2231bed7ce898082b853330ae0228ce9736f995fac63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 KB (34734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef87feab5ce200e7112e4a4585357b48a784179312f35567b704ce21f3fbd61`

```dockerfile
```

-	Layers:
	-	`sha256:d7cdb56e810b0176c955355de60dc1a60ec0eee82383265995bb73eb96b3d8af`  
		Last Modified: Thu, 19 Sep 2024 22:49:22 GMT  
		Size: 34.7 KB (34734 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:54ec71967ac71359ffb9016d95949e70d43fd309bbeef8f93cf346a480a0eaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124364689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47f32ca7830e1aa76c50998372068279873a389d7030779152a29baa3d7f6d2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-x86_64'; 			sha256='cbafe95cca26f77e9271978ad81387dd888eb36e9fdfad3e6fa3b173fcfe9dae'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv6'; 			sha256='3d999fa956f2da65b09584b1052c4cae5d5ea7b68e18dda27061e9eb8edc4150'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-armv7'; 			sha256='0a969be6d781f74248980f9b9e37a053ed9ec8b1a116dfc597510d953d316b70'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-aarch64'; 			sha256='fd39a8ad23303fc079449444a294ea4261f27ed55e22c0fb18a8a55cb550f7e1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-ppc64le'; 			sha256='d2097658b33f4de9840a0a66f77e33acf343b7d0f188c1723bd8bf5ec35aae4e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-riscv64'; 			sha256='a7474c04d13c909783fa785d5890e884905eb581de4cd5e65097354a73351a1a'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-linux-s390x'; 			sha256='b4d7c14cc62356669881e5eb3545d1c4788db59442d48893cada062f2f78f059'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 19 Sep 2024 20:03:59 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD ["sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 19 Sep 2024 20:03:59 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Sep 2024 20:03:59 GMT
VOLUME [/var/lib/docker]
# Thu, 19 Sep 2024 20:03:59 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 19 Sep 2024 20:03:59 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 19 Sep 2024 20:03:59 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac5e2875ced7a97a29ce42c4c829c064ed1e53d3593f1087bdc342fc401b5dd`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 8.0 MB (7981901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9010ef713ffc9216f6ffccc8ee629d7e509dc26203315b4d4560e18c7b590a97`  
		Last Modified: Thu, 19 Sep 2024 21:58:31 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad46c01d2fd1c1ec5d1205e39e1ff8b0ee54ac45e7713175b0459693da6727e6`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.5 MB (17513008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea3fc7d1c32138bf2900f86e16a81b4b81e8e48c58856ad3cb248d28413217e`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 16.8 MB (16800779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98737530f290dc9a951ef64bfbef9b8c3813f7a03543d831d155b62269416809`  
		Last Modified: Thu, 19 Sep 2024 21:58:32 GMT  
		Size: 17.4 MB (17411685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f26fba89eb7c9d87d9b125ab56b7b406d0b75c526903dce3ad6ba749e1af4a0`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e8e87411205d15046fc0e4801b9f562139c6583a7111b294b458d56eaae381`  
		Last Modified: Thu, 19 Sep 2024 21:58:33 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5002185ece7fbd3c72cce3e76f3c8cceb35dc3bc14120b9c91307bcf0697f3`  
		Last Modified: Thu, 19 Sep 2024 21:58:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453ff960fc6f8f7a206ace67ae62cb0608e9b719730268dcbe752223395483`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 7.0 MB (7034934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b42c84695369973183db00dcb7464de237b654c851a03126c9f7ea5f172e0`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 98.7 KB (98657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ebb670570167b85019b9539755dd3d36c21b3b5990092901d78db910326c72`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2908266868416697dbce4c823465148a4268633538e5eecc02b0a69648787851`  
		Last Modified: Thu, 19 Sep 2024 22:49:20 GMT  
		Size: 53.4 MB (53428138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28cf017f7bc6b4a782cc830039a51fc8c510c11c23777adc5890084ba8c9ec`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499680a6cceafce85d9dff164dc5720521e20bb8042e96805d3c5753ba84057`  
		Last Modified: Thu, 19 Sep 2024 22:49:19 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a469f7265f69f428bc4ddaa7bec9ce5f644cd288d43463e84f261c6e9ffa976d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fa4d3e08216860e1a814eafba8c5b4c29dfe6c881f77e87e5df174883219d9`

```dockerfile
```

-	Layers:
	-	`sha256:c56fa241c7c8f1ca9d8fa59cd5c325e03d097bd8c63c20da84d29a40861a9bbc`  
		Last Modified: Thu, 19 Sep 2024 22:49:18 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:2d3e908e028f64af2dc40f03d99afbf47bac68ba78ca11ab817a8fb1aec495f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:2cd33cc5181c44eddcacfa9db5d530579e7766b8574349fdd0fc204ca8009fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:705072809a3097103920e6543769218757c501a38afa6956bf0d1c181ed4b01a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778687122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7f6611b80727958ac8bbd3c1c3e625eb725e938f95a0ac0a9c7929d4402d1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 22:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:26 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:50:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:50:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:50:49 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f217036f9dc172b4ea8832198565611ea81d76cd0a2b7e4c83fff2466588743a`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695aef7398cf5d43a2235c05f4eae468ea2d52cb7100329fe6137fd2aab31d7`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 339.7 KB (339665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e88c5a1af375fedc722906d357bd81a05b4924ac4103e3eae1230f960976ff`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7527df541a965f62694a63e2dc2f0f38efa8efe79c1168ae1abef349b638c461`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0655b558d2401e581e706d3cfb2a7a1f38c3502b1ef48331e3f0da5162db66e0`  
		Last Modified: Thu, 19 Sep 2024 22:51:24 GMT  
		Size: 18.9 MB (18883570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23dd0bccda56adb407a0d46bff04d6a40990d83f70f937f7071c25495368a409`  
		Last Modified: Thu, 19 Sep 2024 22:51:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a274262927d7235ebe21a985b3934f46c51f475b96fbc3f80ec7525fe24f39b1`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc029a63baefdcd4967cd1e81a14b77c202b8343c888f1c4c0cccfcbabaf34d`  
		Last Modified: Thu, 19 Sep 2024 22:51:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f052abd7bb87d9143c2b9a153382aa8ee1e98c605fff15b8fa2b2d5e8da257`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.3 MB (19278342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129644068d7ef2c9e7e6093809be26c2386664b19c4f7bedbe22e6362659dd36`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5aa0fce8cad01b33a4d6491aba8abcd3ba7df8a12a96f089fa0238b264349`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253361ec2ee7a81405952ed3948707b28edb384ab621c7aad66698ebe2e21115`  
		Last Modified: Thu, 19 Sep 2024 22:51:19 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1955f1d42d75eeeb7362a9f6f2651bce5a64c24c28a857c4e135262e31e48b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:22 GMT  
		Size: 19.9 MB (19905392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d436ba51852b1b7153307c438211d920860c7c1f8afe56ff64e0c89ec8eb79c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:79bd3e11b23225a105246d33b69e9fd64e250c9ed22eb4492ee5276371d1c4a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520545613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aaf283596687d47925aafe9d28744df5adb2433d028e43492a14c0731ea9b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 22:49:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 19 Sep 2024 22:50:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 19 Sep 2024 22:50:44 GMT
ENV DOCKER_VERSION=27.3.0
# Thu, 19 Sep 2024 22:50:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.0.zip
# Thu, 19 Sep 2024 22:51:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Thu, 19 Sep 2024 22:51:05 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Thu, 19 Sep 2024 22:51:15 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.6
# Thu, 19 Sep 2024 22:51:16 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.6/docker-compose-windows-x86_64.exe
# Thu, 19 Sep 2024 22:51:17 GMT
ENV DOCKER_COMPOSE_SHA256=0ead495cd4b275bf4988fc04635ee5e603853ff4b494b6dc13c3127fe03919d1
# Thu, 19 Sep 2024 22:51:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a340dae473a2ca2f569f407e3ea8c8f3c7b46c5481ec0f33c1e74e3ae5e9cf`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999e00fc5481bc6bd71cb780265e2fef0388026bef731d04ab45fdd24547516`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 360.9 KB (360939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491419f33e1c86c2f723906ba7adbae6f1ce8e61aa2a2bc79dffbdf25f1cec5f`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12276323809bd0c7bd8016863f9d7c6aa9e7d95b0e66ba0ff1b6faa46730286`  
		Last Modified: Thu, 19 Sep 2024 22:51:31 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e2793bc4f8d8825abf4aabeff1004662213e33decb3db4c2d8c81612c7b48e`  
		Last Modified: Thu, 19 Sep 2024 22:51:33 GMT  
		Size: 18.9 MB (18852010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d4fadcff266fbf0c50d29b18842deab1722f8b9d65c3c5fb84c166ca164836`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e395dabeec55d5bba579c322b09ee2c9abe27e18507765a5f3119892c7a2ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1fba5368f1b18f59628f46b1022cef757b9147c017c99fd8e5c41befebb087`  
		Last Modified: Thu, 19 Sep 2024 22:51:30 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a688db666f6d3d33dadae68bd29335bef813c260fa9f347008ed33e4cc75b4b`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.2 MB (19247713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5876ed6a86e956791e37b3bd112bbb87dc3a1d7c32759f9801b3bc933f0740`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd89e488f97d0fb8cdcb8ab886a53e8cd9ec7a524a6604470477db84f94d57b7`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d0c4c48d04f829a8305ccf8911b26bb9d5fee6dd5f42dc50c46e10cf0dd6ca`  
		Last Modified: Thu, 19 Sep 2024 22:51:29 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4955e1b631502f518f7dd103c60ee31645adc3ac1757cd4152b21553e430256c`  
		Last Modified: Thu, 19 Sep 2024 22:51:32 GMT  
		Size: 19.9 MB (19880947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
