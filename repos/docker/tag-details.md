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
-	[`docker:27.3.1`](#docker2731)
-	[`docker:27.3.1-alpine3.20`](#docker2731-alpine320)
-	[`docker:27.3.1-cli`](#docker2731-cli)
-	[`docker:27.3.1-cli-alpine3.20`](#docker2731-cli-alpine320)
-	[`docker:27.3.1-dind`](#docker2731-dind)
-	[`docker:27.3.1-dind-alpine3.20`](#docker2731-dind-alpine320)
-	[`docker:27.3.1-dind-rootless`](#docker2731-dind-rootless)
-	[`docker:27.3.1-windowsservercore`](#docker2731-windowsservercore)
-	[`docker:27.3.1-windowsservercore-1809`](#docker2731-windowsservercore-1809)
-	[`docker:27.3.1-windowsservercore-ltsc2022`](#docker2731-windowsservercore-ltsc2022)
-	[`docker:cli`](#dockercli)
-	[`docker:dind`](#dockerdind)
-	[`docker:dind-rootless`](#dockerdind-rootless)
-	[`docker:latest`](#dockerlatest)
-	[`docker:windowsservercore`](#dockerwindowsservercore)
-	[`docker:windowsservercore-1809`](#dockerwindowsservercore-1809)
-	[`docker:windowsservercore-ltsc2022`](#dockerwindowsservercore-ltsc2022)

## `docker:27`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:c6d51b0ab67dd257c7c2ad586c1ab9563824fe5ca1c6f6ebb72a315c4f8c762b
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
$ docker pull docker@sha256:4e7fd3a8f93d52916c2346c3356077c6af3f8b62e1af120b1853db58cb68206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67762651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb6abd08343f8be8298144c1a516a263d79fa78ea249cd5d26c5a2596fec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5528133acfc159d367c06dccf347330920e4745168d15cf1374185b0dd55f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be5ccf781f7af49f2a00d9584c82c1944a5ad28385f1029d4f9a6a0969de54`

```dockerfile
```

-	Layers:
	-	`sha256:385e421f46bfde4bddb958c5a9c10070f01f7ac5b833098f3447dd661846b529`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 38.0 KB (37952 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:923c19ad8e666c873723d8412bf9236a7a9ec8c54b62c935e4575c05de135296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a024cba3db5175ab68bf22322c3baf791f20a5d0be64f4e3fab54e7b2d9750d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d5c0d16b88a18f7687bccd1c57500e221af53d8456680189acc663bac96609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf262329a51f905a5847a185fd0b4d5d129733af807f29b9163f6c93813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:17b4a2acfbb68f7f19cb9f9d016de3f8122f8536dfcd88b97c6472aaee720394`  
		Last Modified: Mon, 04 Nov 2024 22:04:02 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bca8c37b10673bbdd065b3f7e1c724b8b89e64297cddde7d9fa22709cecaa13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50608a21f22aa4ebfb24c066b49933be95e192320a47947933a21b232f221b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f2ac1d73a871334997da6eace5056971a05bb63fad8a2c3331c8126bba630b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535a7bfc1731239542c285cae166be15a75dcc7ab70a0e09e4d532f8b5b41f14`

```dockerfile
```

-	Layers:
	-	`sha256:c273b99514ac325aea5e7831a7caf1a0413b278c20e2ed0d7543742786ae5fa4`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:558ddd39f601e73ac32649bed85f131012cd6eb283ec02f56d09d5bff38f3e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:59a038329005fb8643e2d7ec816bd5c2d7ddab0308005c54c380664d0a531a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34920f0054f0dc15893e7ee24f3beefa51aab7bfa00aeda82ea81b44d31b9781`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc589174259db901b77f24c77396ba1cb2d245fc9d63ad46798f2a527243219`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67ddfbcad23d9361fcbbe5ae3aa3cf1a6319f3d52020ce68ec42088b775b22`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599864f326e2c1549900f38b3d6c8459dd3ceaf22af79234a44bf70c277011ea`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c20269725099ad9d9f657afbe4322cd5aa16d13250f430957b459f1c8c0720`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0944e48ae6b9a0cf00868f0baa8405249ea007dd0f287bf468b3ba9cef3ba20`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7435129d2e6c097beaf8ba309abfb45bd64735930bf11f2d1387e2db9a418ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4274bf0c44339a658967d33cf15b0c51e565663dcd97ca8459bab8b791ad5e76`

```dockerfile
```

-	Layers:
	-	`sha256:883c8196b38876bebc58471f6dd1cf53ee6145ff26f595d07e8dcc9232a18674`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18dc60056575ff99d65b9cc6b6148164724c50dd654294c9da31771338184d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf574dd5d7a9e81fa65a776a8af86ed839ce1533afbb393dcebdda4fcff1c0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b243fb6e0391f376f96a59916315be4817b04fc6ae1b77ac79e02bfc4d6210f4`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.0 MB (1023855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4427e773052c12ae322276350fecef6053ec9f332ed4d3d734642557303e3`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34fd3ceae8c8732d0be225b7d646a2b183ef53c246b7e676966c9ad1df7d6b`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c8cfb86d9399605abd45f58f1c64149e5827add58c28a9e7409d6e456a9af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce33ef71682abd24478fd6027d4da5a18ad264faaf9b42b921997b1568e3af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6048b64b84812424d1cdb5ee573e9825bf3f46a5b0c855aebfb286200f412ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298f3cdae05077254b2daee25cb7bf700ffc854fcb2a6bc55a065f73c92c2f56`

```dockerfile
```

-	Layers:
	-	`sha256:a2d138e6d0053942d54953cd6e5ed54156d634d85e9fdbb9ea11241444a3af73`  
		Last Modified: Tue, 05 Nov 2024 01:17:01 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-cli`

```console
$ docker pull docker@sha256:c6d51b0ab67dd257c7c2ad586c1ab9563824fe5ca1c6f6ebb72a315c4f8c762b
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
$ docker pull docker@sha256:4e7fd3a8f93d52916c2346c3356077c6af3f8b62e1af120b1853db58cb68206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67762651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb6abd08343f8be8298144c1a516a263d79fa78ea249cd5d26c5a2596fec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5528133acfc159d367c06dccf347330920e4745168d15cf1374185b0dd55f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be5ccf781f7af49f2a00d9584c82c1944a5ad28385f1029d4f9a6a0969de54`

```dockerfile
```

-	Layers:
	-	`sha256:385e421f46bfde4bddb958c5a9c10070f01f7ac5b833098f3447dd661846b529`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 38.0 KB (37952 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:923c19ad8e666c873723d8412bf9236a7a9ec8c54b62c935e4575c05de135296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a024cba3db5175ab68bf22322c3baf791f20a5d0be64f4e3fab54e7b2d9750d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d5c0d16b88a18f7687bccd1c57500e221af53d8456680189acc663bac96609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf262329a51f905a5847a185fd0b4d5d129733af807f29b9163f6c93813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:17b4a2acfbb68f7f19cb9f9d016de3f8122f8536dfcd88b97c6472aaee720394`  
		Last Modified: Mon, 04 Nov 2024 22:04:02 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bca8c37b10673bbdd065b3f7e1c724b8b89e64297cddde7d9fa22709cecaa13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50608a21f22aa4ebfb24c066b49933be95e192320a47947933a21b232f221b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f2ac1d73a871334997da6eace5056971a05bb63fad8a2c3331c8126bba630b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535a7bfc1731239542c285cae166be15a75dcc7ab70a0e09e4d532f8b5b41f14`

```dockerfile
```

-	Layers:
	-	`sha256:c273b99514ac325aea5e7831a7caf1a0413b278c20e2ed0d7543742786ae5fa4`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind-rootless`

```console
$ docker pull docker@sha256:558ddd39f601e73ac32649bed85f131012cd6eb283ec02f56d09d5bff38f3e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:59a038329005fb8643e2d7ec816bd5c2d7ddab0308005c54c380664d0a531a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34920f0054f0dc15893e7ee24f3beefa51aab7bfa00aeda82ea81b44d31b9781`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc589174259db901b77f24c77396ba1cb2d245fc9d63ad46798f2a527243219`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67ddfbcad23d9361fcbbe5ae3aa3cf1a6319f3d52020ce68ec42088b775b22`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599864f326e2c1549900f38b3d6c8459dd3ceaf22af79234a44bf70c277011ea`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c20269725099ad9d9f657afbe4322cd5aa16d13250f430957b459f1c8c0720`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0944e48ae6b9a0cf00868f0baa8405249ea007dd0f287bf468b3ba9cef3ba20`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7435129d2e6c097beaf8ba309abfb45bd64735930bf11f2d1387e2db9a418ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4274bf0c44339a658967d33cf15b0c51e565663dcd97ca8459bab8b791ad5e76`

```dockerfile
```

-	Layers:
	-	`sha256:883c8196b38876bebc58471f6dd1cf53ee6145ff26f595d07e8dcc9232a18674`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18dc60056575ff99d65b9cc6b6148164724c50dd654294c9da31771338184d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf574dd5d7a9e81fa65a776a8af86ed839ce1533afbb393dcebdda4fcff1c0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b243fb6e0391f376f96a59916315be4817b04fc6ae1b77ac79e02bfc4d6210f4`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.0 MB (1023855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4427e773052c12ae322276350fecef6053ec9f332ed4d3d734642557303e3`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34fd3ceae8c8732d0be225b7d646a2b183ef53c246b7e676966c9ad1df7d6b`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c8cfb86d9399605abd45f58f1c64149e5827add58c28a9e7409d6e456a9af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce33ef71682abd24478fd6027d4da5a18ad264faaf9b42b921997b1568e3af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6048b64b84812424d1cdb5ee573e9825bf3f46a5b0c855aebfb286200f412ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298f3cdae05077254b2daee25cb7bf700ffc854fcb2a6bc55a065f73c92c2f56`

```dockerfile
```

-	Layers:
	-	`sha256:a2d138e6d0053942d54953cd6e5ed54156d634d85e9fdbb9ea11241444a3af73`  
		Last Modified: Tue, 05 Nov 2024 01:17:01 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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

### `docker:27.3.1` - linux; amd64

```console
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-alpine3.20`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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

### `docker:27.3.1-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli`

```console
$ docker pull docker@sha256:c6d51b0ab67dd257c7c2ad586c1ab9563824fe5ca1c6f6ebb72a315c4f8c762b
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

### `docker:27.3.1-cli` - linux; amd64

```console
$ docker pull docker@sha256:4e7fd3a8f93d52916c2346c3356077c6af3f8b62e1af120b1853db58cb68206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67762651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb6abd08343f8be8298144c1a516a263d79fa78ea249cd5d26c5a2596fec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:5528133acfc159d367c06dccf347330920e4745168d15cf1374185b0dd55f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be5ccf781f7af49f2a00d9584c82c1944a5ad28385f1029d4f9a6a0969de54`

```dockerfile
```

-	Layers:
	-	`sha256:385e421f46bfde4bddb958c5a9c10070f01f7ac5b833098f3447dd661846b529`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 38.0 KB (37952 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:923c19ad8e666c873723d8412bf9236a7a9ec8c54b62c935e4575c05de135296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a024cba3db5175ab68bf22322c3baf791f20a5d0be64f4e3fab54e7b2d9750d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d5c0d16b88a18f7687bccd1c57500e221af53d8456680189acc663bac96609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf262329a51f905a5847a185fd0b4d5d129733af807f29b9163f6c93813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:17b4a2acfbb68f7f19cb9f9d016de3f8122f8536dfcd88b97c6472aaee720394`  
		Last Modified: Mon, 04 Nov 2024 22:04:02 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bca8c37b10673bbdd065b3f7e1c724b8b89e64297cddde7d9fa22709cecaa13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50608a21f22aa4ebfb24c066b49933be95e192320a47947933a21b232f221b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:f2ac1d73a871334997da6eace5056971a05bb63fad8a2c3331c8126bba630b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535a7bfc1731239542c285cae166be15a75dcc7ab70a0e09e4d532f8b5b41f14`

```dockerfile
```

-	Layers:
	-	`sha256:c273b99514ac325aea5e7831a7caf1a0413b278c20e2ed0d7543742786ae5fa4`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli-alpine3.20`

```console
$ docker pull docker@sha256:c6d51b0ab67dd257c7c2ad586c1ab9563824fe5ca1c6f6ebb72a315c4f8c762b
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

### `docker:27.3.1-cli-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:4e7fd3a8f93d52916c2346c3356077c6af3f8b62e1af120b1853db58cb68206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67762651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb6abd08343f8be8298144c1a516a263d79fa78ea249cd5d26c5a2596fec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:5528133acfc159d367c06dccf347330920e4745168d15cf1374185b0dd55f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be5ccf781f7af49f2a00d9584c82c1944a5ad28385f1029d4f9a6a0969de54`

```dockerfile
```

-	Layers:
	-	`sha256:385e421f46bfde4bddb958c5a9c10070f01f7ac5b833098f3447dd661846b529`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 38.0 KB (37952 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:923c19ad8e666c873723d8412bf9236a7a9ec8c54b62c935e4575c05de135296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a024cba3db5175ab68bf22322c3baf791f20a5d0be64f4e3fab54e7b2d9750d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:6d5c0d16b88a18f7687bccd1c57500e221af53d8456680189acc663bac96609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf262329a51f905a5847a185fd0b4d5d129733af807f29b9163f6c93813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:17b4a2acfbb68f7f19cb9f9d016de3f8122f8536dfcd88b97c6472aaee720394`  
		Last Modified: Mon, 04 Nov 2024 22:04:02 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bca8c37b10673bbdd065b3f7e1c724b8b89e64297cddde7d9fa22709cecaa13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50608a21f22aa4ebfb24c066b49933be95e192320a47947933a21b232f221b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f2ac1d73a871334997da6eace5056971a05bb63fad8a2c3331c8126bba630b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535a7bfc1731239542c285cae166be15a75dcc7ab70a0e09e4d532f8b5b41f14`

```dockerfile
```

-	Layers:
	-	`sha256:c273b99514ac325aea5e7831a7caf1a0413b278c20e2ed0d7543742786ae5fa4`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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

### `docker:27.3.1-dind` - linux; amd64

```console
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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

### `docker:27.3.1-dind-alpine3.20` - linux; amd64

```console
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-rootless`

```console
$ docker pull docker@sha256:558ddd39f601e73ac32649bed85f131012cd6eb283ec02f56d09d5bff38f3e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:59a038329005fb8643e2d7ec816bd5c2d7ddab0308005c54c380664d0a531a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34920f0054f0dc15893e7ee24f3beefa51aab7bfa00aeda82ea81b44d31b9781`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc589174259db901b77f24c77396ba1cb2d245fc9d63ad46798f2a527243219`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67ddfbcad23d9361fcbbe5ae3aa3cf1a6319f3d52020ce68ec42088b775b22`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599864f326e2c1549900f38b3d6c8459dd3ceaf22af79234a44bf70c277011ea`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c20269725099ad9d9f657afbe4322cd5aa16d13250f430957b459f1c8c0720`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0944e48ae6b9a0cf00868f0baa8405249ea007dd0f287bf468b3ba9cef3ba20`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7435129d2e6c097beaf8ba309abfb45bd64735930bf11f2d1387e2db9a418ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4274bf0c44339a658967d33cf15b0c51e565663dcd97ca8459bab8b791ad5e76`

```dockerfile
```

-	Layers:
	-	`sha256:883c8196b38876bebc58471f6dd1cf53ee6145ff26f595d07e8dcc9232a18674`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18dc60056575ff99d65b9cc6b6148164724c50dd654294c9da31771338184d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf574dd5d7a9e81fa65a776a8af86ed839ce1533afbb393dcebdda4fcff1c0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b243fb6e0391f376f96a59916315be4817b04fc6ae1b77ac79e02bfc4d6210f4`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.0 MB (1023855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4427e773052c12ae322276350fecef6053ec9f332ed4d3d734642557303e3`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34fd3ceae8c8732d0be225b7d646a2b183ef53c246b7e676966c9ad1df7d6b`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c8cfb86d9399605abd45f58f1c64149e5827add58c28a9e7409d6e456a9af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce33ef71682abd24478fd6027d4da5a18ad264faaf9b42b921997b1568e3af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6048b64b84812424d1cdb5ee573e9825bf3f46a5b0c855aebfb286200f412ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298f3cdae05077254b2daee25cb7bf700ffc854fcb2a6bc55a065f73c92c2f56`

```dockerfile
```

-	Layers:
	-	`sha256:a2d138e6d0053942d54953cd6e5ed54156d634d85e9fdbb9ea11241444a3af73`  
		Last Modified: Tue, 05 Nov 2024 01:17:01 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:c6d51b0ab67dd257c7c2ad586c1ab9563824fe5ca1c6f6ebb72a315c4f8c762b
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
$ docker pull docker@sha256:4e7fd3a8f93d52916c2346c3356077c6af3f8b62e1af120b1853db58cb68206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67762651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66eb6abd08343f8be8298144c1a516a263d79fa78ea249cd5d26c5a2596fec2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:5528133acfc159d367c06dccf347330920e4745168d15cf1374185b0dd55f9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23be5ccf781f7af49f2a00d9584c82c1944a5ad28385f1029d4f9a6a0969de54`

```dockerfile
```

-	Layers:
	-	`sha256:385e421f46bfde4bddb958c5a9c10070f01f7ac5b833098f3447dd661846b529`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 38.0 KB (37952 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:78212629afc3e15d183a70f32cf23f8e70704ba283a4f0d00398dd9584279510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62984893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9822d68f013f712019e4b183ece4a11a28fe6c079e602cde9592e91d6f617e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 17:02:10 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-x86_64'; 			sha256='64b798329464b7553bdf4706c5fb1a97dc9504b360f29d30479ac126017d3944'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv6'; 			sha256='a22f58dfc94fd1f8e86dee81e1378ae648c14a3bf0604d3a5434b53650619140'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-armv7'; 			sha256='9fb8f299c55451c08ea04dd7770fd698f45e31ab12df99dd582f0fa0984f5364'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-aarch64'; 			sha256='2c7c902a845288c5733f6d13910ef65e17283f25b3519dee704d6d74de2ec78b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-ppc64le'; 			sha256='a3778d98118d408620eeed110a9bf85c77460601384899566293e8e90e21e206'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-riscv64'; 			sha256='9d3215288f9e9626c4e720576582fedbb4dfa3c728e53e3bb7151eca0251fa5c'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-linux-s390x'; 			sha256='797f3d346f53ffc751eb0bebc9c8f610503bdea84ec993d00ee15e77ed2f0eb9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Nov 2024 17:02:10 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Nov 2024 17:02:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 17:02:10 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3a5eb91c5620b2e792b554b76f6ec9888d39a3ecabcffb8d99c81b5e67ca1`  
		Last Modified: Tue, 05 Nov 2024 20:36:49 GMT  
		Size: 18.0 MB (17961617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e37e56ea8cbb0b9fab757187da560b447cd2d1a890f44355bd2a5099c74422`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3af34626ea298690c7a21326a1c8727a1342f7b33088cfaaa34fd4702a7bfd6`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76871dcfe336f220ab26902cb005fd2029fe26873105146cc449bc95ae1a825`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:2cdbc650689d824c2b7cbb94b0e80caccf7eaa334328351264e108bc2cba3e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486701761074abf98bf9cf755f7313516cfbc2aaa5b1eea00d73a0602de432f2`

```dockerfile
```

-	Layers:
	-	`sha256:d6cc3021aa985167d089e5454348a0070fd3beb046771ac93c49760975478574`  
		Last Modified: Tue, 05 Nov 2024 20:36:48 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:923c19ad8e666c873723d8412bf9236a7a9ec8c54b62c935e4575c05de135296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62008305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a024cba3db5175ab68bf22322c3baf791f20a5d0be64f4e3fab54e7b2d9750d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6d5c0d16b88a18f7687bccd1c57500e221af53d8456680189acc663bac96609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edf262329a51f905a5847a185fd0b4d5d129733af807f29b9163f6c93813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:17b4a2acfbb68f7f19cb9f9d016de3f8122f8536dfcd88b97c6472aaee720394`  
		Last Modified: Mon, 04 Nov 2024 22:04:02 GMT  
		Size: 38.1 KB (38109 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:bca8c37b10673bbdd065b3f7e1c724b8b89e64297cddde7d9fa22709cecaa13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50608a21f22aa4ebfb24c066b49933be95e192320a47947933a21b232f221b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Wed, 30 Oct 2024 23:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 30 Oct 2024 23:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 30 Oct 2024 23:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Oct 2024 23:04:15 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:f2ac1d73a871334997da6eace5056971a05bb63fad8a2c3331c8126bba630b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535a7bfc1731239542c285cae166be15a75dcc7ab70a0e09e4d532f8b5b41f14`

```dockerfile
```

-	Layers:
	-	`sha256:c273b99514ac325aea5e7831a7caf1a0413b278c20e2ed0d7543742786ae5fa4`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 38.2 KB (38152 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:558ddd39f601e73ac32649bed85f131012cd6eb283ec02f56d09d5bff38f3e05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:59a038329005fb8643e2d7ec816bd5c2d7ddab0308005c54c380664d0a531a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157010061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34920f0054f0dc15893e7ee24f3beefa51aab7bfa00aeda82ea81b44d31b9781`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc589174259db901b77f24c77396ba1cb2d245fc9d63ad46798f2a527243219`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67ddfbcad23d9361fcbbe5ae3aa3cf1a6319f3d52020ce68ec42088b775b22`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599864f326e2c1549900f38b3d6c8459dd3ceaf22af79234a44bf70c277011ea`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c20269725099ad9d9f657afbe4322cd5aa16d13250f430957b459f1c8c0720`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 21.3 MB (21303257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0944e48ae6b9a0cf00868f0baa8405249ea007dd0f287bf468b3ba9cef3ba20`  
		Last Modified: Mon, 04 Nov 2024 23:51:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7435129d2e6c097beaf8ba309abfb45bd64735930bf11f2d1387e2db9a418ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4274bf0c44339a658967d33cf15b0c51e565663dcd97ca8459bab8b791ad5e76`

```dockerfile
```

-	Layers:
	-	`sha256:883c8196b38876bebc58471f6dd1cf53ee6145ff26f595d07e8dcc9232a18674`  
		Last Modified: Mon, 04 Nov 2024 23:51:36 GMT  
		Size: 30.6 KB (30617 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18dc60056575ff99d65b9cc6b6148164724c50dd654294c9da31771338184d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151567494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbf574dd5d7a9e81fa65a776a8af86ed839ce1533afbb393dcebdda4fcff1c0`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
USER rootless
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b243fb6e0391f376f96a59916315be4817b04fc6ae1b77ac79e02bfc4d6210f4`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.0 MB (1023855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4427e773052c12ae322276350fecef6053ec9f332ed4d3d734642557303e3`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34fd3ceae8c8732d0be225b7d646a2b183ef53c246b7e676966c9ad1df7d6b`  
		Last Modified: Tue, 05 Nov 2024 01:17:02 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c8cfb86d9399605abd45f58f1c64149e5827add58c28a9e7409d6e456a9af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce33ef71682abd24478fd6027d4da5a18ad264faaf9b42b921997b1568e3af`  
		Last Modified: Tue, 05 Nov 2024 01:17:03 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:6048b64b84812424d1cdb5ee573e9825bf3f46a5b0c855aebfb286200f412ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298f3cdae05077254b2daee25cb7bf700ffc854fcb2a6bc55a065f73c92c2f56`

```dockerfile
```

-	Layers:
	-	`sha256:a2d138e6d0053942d54953cd6e5ed54156d634d85e9fdbb9ea11241444a3af73`  
		Last Modified: Tue, 05 Nov 2024 01:17:01 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:25654f4044cf31ea6ca67707a767c2e7773a5266762aeba44e77307f2166ae2d
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
$ docker pull docker@sha256:3a9f7a6031a62981727ec5486f076b4a4fe70ac5f40fc14f7925a63fa832b038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134723875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c8ffad381c5b9bfa8a988721ee5c08cb9784ccefabffd7bb372e2392235d47`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9aedea3e98ce5a16fe77273b1c1f4c70ba0f5933ab17323fceced17886510`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 7.9 MB (7889541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b4a3fba9d5ba995eb36588ef2e0d19875ef3dc44b0a5ee681c32835bdf80b4`  
		Last Modified: Mon, 04 Nov 2024 22:03:58 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c043745cf721a68464e7711984582db86b2d6aeea7f9549b5dc6346a3e7cb0a0`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18563415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9734980140e172d48751e7a96317062c23c4a94a4892735d36ab9edf4f3b6406`  
		Last Modified: Mon, 04 Nov 2024 22:03:59 GMT  
		Size: 18.6 MB (18566642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac7bb89f6a806c803dd7c6504fa528da10523973ce5186a349a422e95311139`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b45bb63a72afeec92cec10a591f00d6df27c67ae8f9ff56fe54ea338a11e6`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5583c651d36be9687a804cfee82b31d4546ba22fbebdd5f5e481ba79924257b3`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5d76a3bb7409c9b4a010424c2cd2a9385377b7a12e851cfa72480b453d06e`  
		Last Modified: Mon, 04 Nov 2024 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9b0e0715daf982163adbc5882b37f0846823a4ad5e8812681f14e900a8caaf`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 9.1 MB (9067216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d29528025061881634c084fea45b911802ff1353cbd17cfe545fee325e1d87`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 89.2 KB (89232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ff3db654dba9e83a314c2bc0eddfbbc0df618f18fdac9c642fa760b45397a`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f60e57e2ac1e7ce6555aaf43433a3fe549aceb3623d4f3ee97e19d1a1f21eb`  
		Last Modified: Mon, 04 Nov 2024 23:06:43 GMT  
		Size: 57.8 MB (57798983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aba394b098eddb391e04864dfb680b3059fa76f9ae92bb9822d5b94a97ba2`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3251b2b85aa01466768b72a133ba83db866310d3c68aec0f6fe4e09358f75c`  
		Last Modified: Mon, 04 Nov 2024 23:06:42 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:7ae9e4193359ef7a4e90b307ecfe940b6cb88382b0cd741bbdbbf80aa9eda52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f4a1b0b34b1978406a5c0cce7795881b3c02c64c6bd702e9439f788ada4ef1`

```dockerfile
```

-	Layers:
	-	`sha256:fa9d18b87558c68aa97a931a03a20faad808b246f805bf9757ca2f650c70701e`  
		Last Modified: Mon, 04 Nov 2024 23:06:41 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:101741943c22ae71ed22f76928063e8a2bee680a6f991c63f340f01df6516e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125648575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a836833273383aba31cc4d48ef546717b17f710ae412417f5c2fbe586f913114`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
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
	-	`sha256:fb465bb1c99223887dda92712b33166cd4a60b1d36ed4de3d19a6fdd0643d07c`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 16.6 MB (16601555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467ef678d76541a90258e619a961c4c2969d607944c5af919515f1da0256ab17`  
		Last Modified: Mon, 04 Nov 2024 22:03:35 GMT  
		Size: 17.2 MB (17245299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3906381ff513b7c5f690af41bf60c5ca527b6684bab5276cd23bc3ba2ea94d`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 18.0 MB (17959746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50270769e6db55e09047db2c66f87b2938452bc90b35a7d2b62cb9c5ccb4bac`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67c3306bb2a840b8313e62ac99e4292fba2d7f244db9aa2eea1b4a6a54b4695`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c5119717905f06c66637f2ec9ab89b123507483aa9ced0a909cf72f0e82bb`  
		Last Modified: Mon, 04 Nov 2024 22:03:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46177243157ca85c9ebed603e3aa66d4d7e9e942e1a2933da532708463f50128`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 9.1 MB (9060325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c77a8bc70f86c51d7d86665c3f9815349d9351faca1c873b7b4b278318be7a`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 88.4 KB (88404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eeacbfbf15a32e1137ffd2a7985c10d0d8ed1410b4e732f7902dd7ce53d17b`  
		Last Modified: Mon, 04 Nov 2024 23:06:34 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98e6fe6346c9939c60ae7b9b35d5cd2a2f1b44b7e4197e1c885d603604eb961`  
		Last Modified: Mon, 04 Nov 2024 23:06:36 GMT  
		Size: 53.5 MB (53511026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1154e62b87e2daf9101baee80fec6a8cf7654093021f741573d5267e07a6c4fa`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2abc73f7283d5be9672d403e1a2342ffbbe43eb2b2ea087adefa0e8b2628af5`  
		Last Modified: Mon, 04 Nov 2024 23:06:35 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:b3332b750284faf51e7157d0d4971aa4347b4dcf924b33abb0670eb0cda766f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de652c73ba33214102c916a4800139771912ab62526bc2f0d5dd227b51bab5fd`

```dockerfile
```

-	Layers:
	-	`sha256:0903671526f1204d15c89239d6c26097589866854bf6de095bb9d744a95a467b`  
		Last Modified: Mon, 04 Nov 2024 23:06:33 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:24174e3e5267570f785e1cc387330309020972ddb92f9c272064ee3504f17d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.8 MB (123837980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b573c07cb8aa67e2bc869b7c0939152f8fb66431f01e3a9320e067039fe1367a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad9630fb073cc728b48cd040c68f6c38cbee058b67dec3fbf67a8aabefee293`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 7.2 MB (7153113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d861c44151da828172260c439960b1c88cb8f6a12311e21400f2be72ea99ba`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec6aa66cdea2ed7e99b31bd2d23d867fc4dfcb0f3b5529acd7e9ab83f470eef`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 16.6 MB (16591537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e54c95a41f8d61a774c0c10697398b7efa9aa8f3cc0bac14ad1b2653c96f3d`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.2 MB (17226831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8bb0d4626726066c548c4b9a944a0ee64d45e8084dedb5e42f5921a1aebb9`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 17.9 MB (17939159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f6d313f890a2437bfc7fa1592e6368ac021a4fba2659828c262db479283508`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ebbf04115aa891411149501c3975c9f4f16a16dd1ca868fb628a08035bc5a2`  
		Last Modified: Mon, 04 Nov 2024 22:04:03 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df420f168afc72455447285cf1175f57f23c5930f3b5e9cd3a1affd9de497fb6`  
		Last Modified: Mon, 04 Nov 2024 22:04:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf316dab1d592ae4ccee90ec458994be798f9abeeb9b1ae0fc16009c67efa18`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 8.2 MB (8228340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe15e9751db37bf2b9c786c803f8a50d48d85cdb5ec242a9afdd5844b756ff`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 84.5 KB (84513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7c0bb5888a21af5e5a7f8e0d800829537374f465512fd311c81611adc0b95f`  
		Last Modified: Mon, 04 Nov 2024 23:12:24 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30914a28886555f5fbe17ab3469cc79059f02fd7c4916dabdf0dafbca2e886d`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c98546c4391eb576773c84588443bb896e2dc68ceccbd7689f143f920c146`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 1.5 KB (1515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c745b416d8ddd1c838ec9ea95905fb7d1c36d6a5a71873e21fd3d6e28b27441`  
		Last Modified: Mon, 04 Nov 2024 23:12:25 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:01a1ed8671e75033a312c7671d8b88aefb84c0345d911e9fc05e7a156507466d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1323efa7b5286fd67c9f1f50399d247e6f966d8cbfe021125aad86b015469397`

```dockerfile
```

-	Layers:
	-	`sha256:94ba511b0601808eedcecc069d0b5fb3df0f50ec49712ded09a02d0ea3a04c9a`  
		Last Modified: Mon, 04 Nov 2024 23:12:23 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f1d2fcdbda15f328721f94d04a82649c979488a82cda0ff6678e3044ee55ae5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127386854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9892442e7e9471ed7e57163e7b58bd73bf4ac6efbfca032615a95d97998ec17`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_VERSION=27.3.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-x86_64'; 			sha256='bd976a501e471c14b320876686f1628db3c37ab223405d2a815022fc711e704e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv6'; 			sha256='2c70bd6e01ceb550d81a1bb0981f8f24c58ec301ac0c1432db132e07842544fe'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-armv7'; 			sha256='205f947e00fdfb2d4787fb5d38267d56e68bbf07757d8e30d7b1c9c1086c8477'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-aarch64'; 			sha256='f869d0900f8744b3f295c5bf8ed68488110598891d3db1d93db7203db9fa535b'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-ppc64le'; 			sha256='93e47b53fcaaa366555cfa92ff49c77c16e2d76ccf26f816db24683b6bdb36ac'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-riscv64'; 			sha256='0431d523628c26e74308be72205d13866bc978970b2e98efc60f5ecf23089ed2'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-linux-s390x'; 			sha256='afed38f2f18219d3fe79f2f0bc11d21458195c7f19d812c3ecd1a2608094fa84'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 20 Sep 2024 18:21:55 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD ["sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
VOLUME [/var/lib/docker]
# Fri, 20 Sep 2024 18:21:55 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 20 Sep 2024 18:21:55 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 20 Sep 2024 18:21:55 GMT
CMD []
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed9359514fe81c419d3534f699326195767f31bd79f08455a3a6f20afd5fce`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa02bface670aa4b3e5f2129cd65cd0002596db3f83875d8398e53b158e5ec54`  
		Last Modified: Mon, 04 Nov 2024 22:04:36 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a497c133afd8d70c19f818965e870a689c95a1adc66ea32fd7e64e54235e8156`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17513983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4f43e2e2901f02786c540b1700a8fd93dea28d3da154afd7a8c6b4124c9bc4`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 16.9 MB (16905175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595b2632cbb49739a40b19eb0a8fd74d2ea691b2c2329b5a8868883a47d7499`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 17.5 MB (17492702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d70e0f143c0259f59407533460a8eb5b1ea478cd56fc21d65fd3a75b562fb1`  
		Last Modified: Mon, 04 Nov 2024 22:04:37 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bffc31408e66bc4b2965a3eb87752e15e054364598b2153bef4d74051895d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80116254b4cb1ded9f161d51ee74662b335872d4ac8a51d274fd3f730e5ffe`  
		Last Modified: Mon, 04 Nov 2024 22:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543fc443324e2944351f2b5b3eaef760f6b4173de3a0dd9cb1f2958eb0beb04e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 9.9 MB (9854939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549742acbb4c2b1906dbf75a2587f9689905bb79be274db38d8a019aa0ec3710`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 98.7 KB (98651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543a577564370aebcf599269a9b052a739ce57b83690c242f74b54c2c2ec7da`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46438dddb2ffbb46a44e082038711c7911115d0afa2c28cde57dda083505a5e9`  
		Last Modified: Mon, 04 Nov 2024 23:34:19 GMT  
		Size: 53.4 MB (53428170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7deaa944fa16c098de445d82231c5caa12eb5b79f9fc2dea2e0f27437920aa9e`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b609f1e673c41d032f6176ab132826b468847165c77da4de8d77f43c1bd29`  
		Last Modified: Mon, 04 Nov 2024 23:34:18 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:1cf54ce2bfae4b219062f0bf7e7d1b821621bd692b2fea261a245e70d7ca6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be4a1a1ab979739342406d2a0e191226042764edf7ee3edd1f17c5a5f1af0b0`

```dockerfile
```

-	Layers:
	-	`sha256:a45b5cfa56c82cf817f5ad7bc738e833334f4a1d9d8837480b6f38bdee040058`  
		Last Modified: Mon, 04 Nov 2024 23:34:17 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:cd28bf3a2e7baf7870db5297557509e5f2b6d0b3606056da14b8ec1fa7a63f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:53d0f82df0671a80bac71813cd6239f2c6c24be10aad68ee6b51b935ff629e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1a35ca61678319e7fa93888ef0c4b6e4709e48fce95840b91ce461b4fb68c0f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e192f4fa84e41b105b4d8f1f8be08ad714206e9b895427d8454863abdf781a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 05 Nov 2024 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:37:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:37:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:38:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:38:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:38:05 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:38:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:38:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:38:18 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:38:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4813b36e7d881a8c0916831e96a2aab5bb14a970b4511c40b50dc6ea549c4b`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769d3d822227a2e218750c27cfd87e797ce80220ac6f4cc38a03e51099653f4`  
		Last Modified: Tue, 05 Nov 2024 20:38:38 GMT  
		Size: 486.0 KB (485962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7487cbd079dc170785d605cd0f68071bf38025eeb6d38b7d43de5890eea14cc`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681ea29d0caee8cc10f88b1cc0489d13614f34b008909b60cc06fed0a55251d`  
		Last Modified: Tue, 05 Nov 2024 20:38:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c627cfeb572ebc30978041a968f303246d58cfa014e69e878a755d7e79c1e`  
		Last Modified: Tue, 05 Nov 2024 20:38:37 GMT  
		Size: 18.9 MB (18882040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0cf216d2773a815c028f47e95f99108023a3cb4095f7d7617aff8d9960cc92`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da76889772a7e9f4fbb4c26717ed310e3733574ef6c3f0b38f3bfbf7e850ebf8`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2111de71d8d1835274ec5df193dc2502ed4107b3177b4d26702bba52a59eae9`  
		Last Modified: Tue, 05 Nov 2024 20:38:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32417742f0b230d7b25c7247aa81fec4825f51315a5b50df8cc57cd93feddbe`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 19.4 MB (19403887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857c7a89698ebd86281bbf4feeddd3ebee165f8ba726796215ededb5c053953b`  
		Last Modified: Tue, 05 Nov 2024 20:38:33 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9a45b5a39db991288a5b92a310ea53f0925b559bb7d385f0942bdeb137cb99`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5e0ee45088fe37c634f45e67a99cafde4f0c35edc1ab3f87323d2c119d5d9`  
		Last Modified: Tue, 05 Nov 2024 20:38:32 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cb56365e545fb5bc91339664a9b6b0d340e9f92a284de46e82f6922d8682e5`  
		Last Modified: Tue, 05 Nov 2024 20:38:35 GMT  
		Size: 20.0 MB (19977048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:832a0973a728b261599f8aad5ef361bfd16999d86ecf9ed3e206aff94e57af70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:821e396fc9c1e641f28c174a3788d3fa7e3efa62047213a1dff18211601af9a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858139205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effb370e5455b4936176664113504a55e3450c33d7f2fd3c441eb5bbcbc5973`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 05 Nov 2024 20:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Nov 2024 20:36:55 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 05 Nov 2024 20:36:56 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 05 Nov 2024 20:37:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:12 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Tue, 05 Nov 2024 20:37:13 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Tue, 05 Nov 2024 20:37:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.2
# Tue, 05 Nov 2024 20:37:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.2/docker-compose-windows-x86_64.exe
# Tue, 05 Nov 2024 20:37:23 GMT
ENV DOCKER_COMPOSE_SHA256=c9d3cfb7b2781fae4d2f5bc3cab2cf38ce6e2b48e4d98305c60535f9e3c879d3
# Tue, 05 Nov 2024 20:37:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5eddb602423478d1ea4603ebd5d6b89b2e747cf503f203847816b91277a87`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599ecb111e12b3955957a5d3437d25977a3bc0a592e2c23a8005f69d531650f8`  
		Last Modified: Tue, 05 Nov 2024 20:37:40 GMT  
		Size: 491.7 KB (491730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d60808420b0ffb82c303d784b15b5ee011f8b981964a31f994ddc00af00267`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b530a771b104cf041d5f5d2469be09c2b7cc4c4a2a54d26d410d1f3d95758c94`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003cc952c0899bca38be35be6b6cbfab282efdc71554a3d7341fdaf7a8c8b6e7`  
		Last Modified: Tue, 05 Nov 2024 20:37:39 GMT  
		Size: 18.9 MB (18887448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40084c7bb58d3c98fd6e3e319151f3114ba6965e21ab6dbee5329c441cfef88a`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a239b276f60b9e2ef96f737d42b6cabba0b428f18c01892d9a391fce3bd4076e`  
		Last Modified: Tue, 05 Nov 2024 20:37:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b96aa1bc15b228700eadbd9a68c54d87f4ccbe74ea039633ede0f4bb143dc0`  
		Last Modified: Tue, 05 Nov 2024 20:37:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b989ca69ef5e2b92c5a97121c9081a8c0cf131b36cb2e0df2c72325b914879`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 19.4 MB (19412391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f9195d45fa0b6aaa59a117e3a12a680e6d3b4fd2772e522267889a9fb86e8f`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc371d4ebf8cbdea3eb83f4d1062b266bff4edb6d6fe2695aebe116af4185dd`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2ad99bc62d19dd371cfc63291cd44e40b5e8f0da3b0fd444eba49d2a2088b8`  
		Last Modified: Tue, 05 Nov 2024 20:37:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac536e953382c1faf21a47b074c65aee4a0acb92827fe557a35b049bc415583`  
		Last Modified: Tue, 05 Nov 2024 20:37:38 GMT  
		Size: 20.0 MB (19994400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
