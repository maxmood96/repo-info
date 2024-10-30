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
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:a306852d26bd49b91723c0384f8dbccd5332b32e891f026135de87f8b08678c0
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
$ docker pull docker@sha256:d681001b65c02149db1800056f3e8dd04c46ba0af7cb9c4d9aea4466b83dc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67634487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b8a9636b980903f8dedee7362d64da168948fe9de688eb1eb323b9af3c8773`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0a1bfd10bc1592a1a5bdb1188ff22e5c6a82e5bb369673c1f06e473fd04ffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bf0b3949291682be4fe1f8db801b2ae028f60dbb1657a4dedf8804aa2d85c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb0079f2ad11a0540560cb6484f23edc1707fc7d87c4f30b45961b884f580dc`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3230a03c4ca073df26ebbaba870d46bc674f8b2e32ba6d2f82f89a6f325ffcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62881859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c059726e7ebd5080e0ca6f4218727b1d2e53686342e38bc27f96dd1168be019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:956cbc52d49a237bd08951e7b9637f517528fc3326363ac6524657a16dc50c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbded9c7d487f194e8c3336ae42ac1c523ffe252aa26dd9fb31257198d84b0`

```dockerfile
```

-	Layers:
	-	`sha256:960aabcea856bd351dedf020ec8ddaa7c9413012e686f7603a12d7cc4a12d40a`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eff9e2652593c1611264664a498725555be7f6ff83d2e06481b2122256bfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83e7723a53437758b6b2f1cb88adb5540488fe5c7b5890bb67cb0088247861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1f2ea61961e414563265f4ba7c8d26f925684ae2644051145ceaf20e29c21f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b308c6f1b37816261ed8836666b71f7298aeeedba7790a3a230fa9e07f4fea`

```dockerfile
```

-	Layers:
	-	`sha256:2f81dc59dd0ec7406711323017f2226cad9b01517f4bac6e113cbd58f7caa9de`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:154c7e471b3febf9fa66f77faa913357e19249b582ad27a0328d3646430f0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c219c1d64de3adbc85c883284055b930aa729cd53ad11ceef3c601e814fd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04f0aae5aeb3b0a8dcf632384f22c0c32661dfb9be71fcec4502a8f9ff358d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78f90e01542faa4709016d39f5a2cd153e9bf893f752a51273713b146f6776`

```dockerfile
```

-	Layers:
	-	`sha256:8285d485a74cb3a9d489ff2efd03aa2e3411cb17a6cb42cbc927264a5820d076`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:d7f70287009a765ce9728d09ae0e1ef10ba2451ee7711298a3937da22dd1be5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:97316936aeccbcfae31c3ee8c744d6517a12ee5278ac04728221b7e239291fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b77c63afb3f34de27d291e46c605e0bd7afcd078b2e94c5d7e987b573ba2e79`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7c1b27cb672d81ee0e4513235c74e879beb8a1f41f90268f660474d36731c`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81f22ddfe7fe47f5e6cc0d8b061586e9bfb03d6a0f9a72919fb92e33cd59ee`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceb4b6852f66befe9b5f8c95412a41876132a80328dbdabbd31e81824ad0fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05fd523513dfcd7ea96faec1283dcd08014ade10ca9180907f4dd5337c774b`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 21.3 MB (21303265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc448d15ea248565c3b89094a50084e2f3eded7d9e10e06475223eb1af7a88`  
		Last Modified: Wed, 30 Oct 2024 00:47:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a071ebd27917f7d76a4782c16e2ee0c723cc0317334b4d40159700599dd079b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ed03e7637322aed785abe25aea41b8ebd0c9eac3dd6cd2682ea08d2d40a1`

```dockerfile
```

-	Layers:
	-	`sha256:ce55096dbabb40d46c9d04d1608c3f83e5f81604737859d3977b34896e8ae345`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2018bf77ef9956bea679d229e86a0869408918e0c30acbc4557dd6f80054f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151462614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523b102871ed5328ab73a83b6c7007ebe05f5c35c50847019b01818de3303040`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f11fb7c9a7e46e95a9874adf87e8bafd06bb374be2c74d9ccb4622770585fb`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 MB (1023842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211e328766d831433385aa9924c089cb0c332a4ed3171aacd3a97de972d5053`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f743305622d792bd249ad20ffdcebea86c516bb417c4a66762aaacc3f242638`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a168fb4569ec560dd604ca7e06e9a599446e1ebab8434667345f29399fbd6`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318a4093bafc2dc1e678e46e5fd0d9b285777696e0d2be28d06cfe1521a5bdc`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:24d9a91db2e3210efb574de176582c85aecc21e44e45d2eaf780eb384d5f94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f318787d6f843598fedc7cbfd1b4352e791d42d9506c520cc3af7c1cd448e45`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f847a2eece9d610a02c1a0b9b474079c6f67184588b56f7f3dccbb52bf331`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:2b808b9cad9d1cf6d10e1b0098f5404a87d37ac253fa50c0839772ccde6745c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:134ee55063a0ce1e9ae80e14e7d4412d40320285f3e74dd116773ef49492047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fa70560d32c3309dd4f2ad8d06fc8381d9b8b61f718308e9c54ca5a212272d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-cli`

```console
$ docker pull docker@sha256:a306852d26bd49b91723c0384f8dbccd5332b32e891f026135de87f8b08678c0
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
$ docker pull docker@sha256:d681001b65c02149db1800056f3e8dd04c46ba0af7cb9c4d9aea4466b83dc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67634487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b8a9636b980903f8dedee7362d64da168948fe9de688eb1eb323b9af3c8773`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0a1bfd10bc1592a1a5bdb1188ff22e5c6a82e5bb369673c1f06e473fd04ffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bf0b3949291682be4fe1f8db801b2ae028f60dbb1657a4dedf8804aa2d85c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb0079f2ad11a0540560cb6484f23edc1707fc7d87c4f30b45961b884f580dc`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3230a03c4ca073df26ebbaba870d46bc674f8b2e32ba6d2f82f89a6f325ffcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62881859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c059726e7ebd5080e0ca6f4218727b1d2e53686342e38bc27f96dd1168be019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:956cbc52d49a237bd08951e7b9637f517528fc3326363ac6524657a16dc50c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbded9c7d487f194e8c3336ae42ac1c523ffe252aa26dd9fb31257198d84b0`

```dockerfile
```

-	Layers:
	-	`sha256:960aabcea856bd351dedf020ec8ddaa7c9413012e686f7603a12d7cc4a12d40a`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eff9e2652593c1611264664a498725555be7f6ff83d2e06481b2122256bfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83e7723a53437758b6b2f1cb88adb5540488fe5c7b5890bb67cb0088247861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1f2ea61961e414563265f4ba7c8d26f925684ae2644051145ceaf20e29c21f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b308c6f1b37816261ed8836666b71f7298aeeedba7790a3a230fa9e07f4fea`

```dockerfile
```

-	Layers:
	-	`sha256:2f81dc59dd0ec7406711323017f2226cad9b01517f4bac6e113cbd58f7caa9de`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:154c7e471b3febf9fa66f77faa913357e19249b582ad27a0328d3646430f0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c219c1d64de3adbc85c883284055b930aa729cd53ad11ceef3c601e814fd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04f0aae5aeb3b0a8dcf632384f22c0c32661dfb9be71fcec4502a8f9ff358d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78f90e01542faa4709016d39f5a2cd153e9bf893f752a51273713b146f6776`

```dockerfile
```

-	Layers:
	-	`sha256:8285d485a74cb3a9d489ff2efd03aa2e3411cb17a6cb42cbc927264a5820d076`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind-rootless`

```console
$ docker pull docker@sha256:d7f70287009a765ce9728d09ae0e1ef10ba2451ee7711298a3937da22dd1be5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:97316936aeccbcfae31c3ee8c744d6517a12ee5278ac04728221b7e239291fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b77c63afb3f34de27d291e46c605e0bd7afcd078b2e94c5d7e987b573ba2e79`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7c1b27cb672d81ee0e4513235c74e879beb8a1f41f90268f660474d36731c`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81f22ddfe7fe47f5e6cc0d8b061586e9bfb03d6a0f9a72919fb92e33cd59ee`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceb4b6852f66befe9b5f8c95412a41876132a80328dbdabbd31e81824ad0fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05fd523513dfcd7ea96faec1283dcd08014ade10ca9180907f4dd5337c774b`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 21.3 MB (21303265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc448d15ea248565c3b89094a50084e2f3eded7d9e10e06475223eb1af7a88`  
		Last Modified: Wed, 30 Oct 2024 00:47:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a071ebd27917f7d76a4782c16e2ee0c723cc0317334b4d40159700599dd079b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ed03e7637322aed785abe25aea41b8ebd0c9eac3dd6cd2682ea08d2d40a1`

```dockerfile
```

-	Layers:
	-	`sha256:ce55096dbabb40d46c9d04d1608c3f83e5f81604737859d3977b34896e8ae345`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2018bf77ef9956bea679d229e86a0869408918e0c30acbc4557dd6f80054f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151462614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523b102871ed5328ab73a83b6c7007ebe05f5c35c50847019b01818de3303040`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f11fb7c9a7e46e95a9874adf87e8bafd06bb374be2c74d9ccb4622770585fb`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 MB (1023842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211e328766d831433385aa9924c089cb0c332a4ed3171aacd3a97de972d5053`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f743305622d792bd249ad20ffdcebea86c516bb417c4a66762aaacc3f242638`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a168fb4569ec560dd604ca7e06e9a599446e1ebab8434667345f29399fbd6`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318a4093bafc2dc1e678e46e5fd0d9b285777696e0d2be28d06cfe1521a5bdc`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:24d9a91db2e3210efb574de176582c85aecc21e44e45d2eaf780eb384d5f94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f318787d6f843598fedc7cbfd1b4352e791d42d9506c520cc3af7c1cd448e45`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f847a2eece9d610a02c1a0b9b474079c6f67184588b56f7f3dccbb52bf331`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-windowsservercore`

```console
$ docker pull docker@sha256:2b808b9cad9d1cf6d10e1b0098f5404a87d37ac253fa50c0839772ccde6745c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-1809`

```console
$ docker pull docker@sha256:134ee55063a0ce1e9ae80e14e7d4412d40320285f3e74dd116773ef49492047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fa70560d32c3309dd4f2ad8d06fc8381d9b8b61f718308e9c54ca5a212272d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-alpine3.20`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli`

```console
$ docker pull docker@sha256:a306852d26bd49b91723c0384f8dbccd5332b32e891f026135de87f8b08678c0
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
$ docker pull docker@sha256:d681001b65c02149db1800056f3e8dd04c46ba0af7cb9c4d9aea4466b83dc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67634487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b8a9636b980903f8dedee7362d64da168948fe9de688eb1eb323b9af3c8773`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0a1bfd10bc1592a1a5bdb1188ff22e5c6a82e5bb369673c1f06e473fd04ffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bf0b3949291682be4fe1f8db801b2ae028f60dbb1657a4dedf8804aa2d85c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb0079f2ad11a0540560cb6484f23edc1707fc7d87c4f30b45961b884f580dc`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3230a03c4ca073df26ebbaba870d46bc674f8b2e32ba6d2f82f89a6f325ffcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62881859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c059726e7ebd5080e0ca6f4218727b1d2e53686342e38bc27f96dd1168be019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:956cbc52d49a237bd08951e7b9637f517528fc3326363ac6524657a16dc50c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbded9c7d487f194e8c3336ae42ac1c523ffe252aa26dd9fb31257198d84b0`

```dockerfile
```

-	Layers:
	-	`sha256:960aabcea856bd351dedf020ec8ddaa7c9413012e686f7603a12d7cc4a12d40a`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eff9e2652593c1611264664a498725555be7f6ff83d2e06481b2122256bfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83e7723a53437758b6b2f1cb88adb5540488fe5c7b5890bb67cb0088247861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:1f2ea61961e414563265f4ba7c8d26f925684ae2644051145ceaf20e29c21f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b308c6f1b37816261ed8836666b71f7298aeeedba7790a3a230fa9e07f4fea`

```dockerfile
```

-	Layers:
	-	`sha256:2f81dc59dd0ec7406711323017f2226cad9b01517f4bac6e113cbd58f7caa9de`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:154c7e471b3febf9fa66f77faa913357e19249b582ad27a0328d3646430f0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c219c1d64de3adbc85c883284055b930aa729cd53ad11ceef3c601e814fd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:04f0aae5aeb3b0a8dcf632384f22c0c32661dfb9be71fcec4502a8f9ff358d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78f90e01542faa4709016d39f5a2cd153e9bf893f752a51273713b146f6776`

```dockerfile
```

-	Layers:
	-	`sha256:8285d485a74cb3a9d489ff2efd03aa2e3411cb17a6cb42cbc927264a5820d076`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli-alpine3.20`

```console
$ docker pull docker@sha256:a306852d26bd49b91723c0384f8dbccd5332b32e891f026135de87f8b08678c0
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
$ docker pull docker@sha256:d681001b65c02149db1800056f3e8dd04c46ba0af7cb9c4d9aea4466b83dc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67634487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b8a9636b980903f8dedee7362d64da168948fe9de688eb1eb323b9af3c8773`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:c0a1bfd10bc1592a1a5bdb1188ff22e5c6a82e5bb369673c1f06e473fd04ffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bf0b3949291682be4fe1f8db801b2ae028f60dbb1657a4dedf8804aa2d85c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb0079f2ad11a0540560cb6484f23edc1707fc7d87c4f30b45961b884f580dc`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:3230a03c4ca073df26ebbaba870d46bc674f8b2e32ba6d2f82f89a6f325ffcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62881859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c059726e7ebd5080e0ca6f4218727b1d2e53686342e38bc27f96dd1168be019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:956cbc52d49a237bd08951e7b9637f517528fc3326363ac6524657a16dc50c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbded9c7d487f194e8c3336ae42ac1c523ffe252aa26dd9fb31257198d84b0`

```dockerfile
```

-	Layers:
	-	`sha256:960aabcea856bd351dedf020ec8ddaa7c9413012e686f7603a12d7cc4a12d40a`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eff9e2652593c1611264664a498725555be7f6ff83d2e06481b2122256bfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83e7723a53437758b6b2f1cb88adb5540488fe5c7b5890bb67cb0088247861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:1f2ea61961e414563265f4ba7c8d26f925684ae2644051145ceaf20e29c21f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b308c6f1b37816261ed8836666b71f7298aeeedba7790a3a230fa9e07f4fea`

```dockerfile
```

-	Layers:
	-	`sha256:2f81dc59dd0ec7406711323017f2226cad9b01517f4bac6e113cbd58f7caa9de`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-cli-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:154c7e471b3febf9fa66f77faa913357e19249b582ad27a0328d3646430f0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c219c1d64de3adbc85c883284055b930aa729cd53ad11ceef3c601e814fd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:04f0aae5aeb3b0a8dcf632384f22c0c32661dfb9be71fcec4502a8f9ff358d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78f90e01542faa4709016d39f5a2cd153e9bf893f752a51273713b146f6776`

```dockerfile
```

-	Layers:
	-	`sha256:8285d485a74cb3a9d489ff2efd03aa2e3411cb17a6cb42cbc927264a5820d076`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-rootless`

```console
$ docker pull docker@sha256:d7f70287009a765ce9728d09ae0e1ef10ba2451ee7711298a3937da22dd1be5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:97316936aeccbcfae31c3ee8c744d6517a12ee5278ac04728221b7e239291fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b77c63afb3f34de27d291e46c605e0bd7afcd078b2e94c5d7e987b573ba2e79`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7c1b27cb672d81ee0e4513235c74e879beb8a1f41f90268f660474d36731c`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81f22ddfe7fe47f5e6cc0d8b061586e9bfb03d6a0f9a72919fb92e33cd59ee`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceb4b6852f66befe9b5f8c95412a41876132a80328dbdabbd31e81824ad0fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05fd523513dfcd7ea96faec1283dcd08014ade10ca9180907f4dd5337c774b`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 21.3 MB (21303265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc448d15ea248565c3b89094a50084e2f3eded7d9e10e06475223eb1af7a88`  
		Last Modified: Wed, 30 Oct 2024 00:47:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a071ebd27917f7d76a4782c16e2ee0c723cc0317334b4d40159700599dd079b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ed03e7637322aed785abe25aea41b8ebd0c9eac3dd6cd2682ea08d2d40a1`

```dockerfile
```

-	Layers:
	-	`sha256:ce55096dbabb40d46c9d04d1608c3f83e5f81604737859d3977b34896e8ae345`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2018bf77ef9956bea679d229e86a0869408918e0c30acbc4557dd6f80054f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151462614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523b102871ed5328ab73a83b6c7007ebe05f5c35c50847019b01818de3303040`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f11fb7c9a7e46e95a9874adf87e8bafd06bb374be2c74d9ccb4622770585fb`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 MB (1023842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211e328766d831433385aa9924c089cb0c332a4ed3171aacd3a97de972d5053`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f743305622d792bd249ad20ffdcebea86c516bb417c4a66762aaacc3f242638`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a168fb4569ec560dd604ca7e06e9a599446e1ebab8434667345f29399fbd6`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318a4093bafc2dc1e678e46e5fd0d9b285777696e0d2be28d06cfe1521a5bdc`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:24d9a91db2e3210efb574de176582c85aecc21e44e45d2eaf780eb384d5f94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f318787d6f843598fedc7cbfd1b4352e791d42d9506c520cc3af7c1cd448e45`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f847a2eece9d610a02c1a0b9b474079c6f67184588b56f7f3dccbb52bf331`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-windowsservercore`

```console
$ docker pull docker@sha256:2b808b9cad9d1cf6d10e1b0098f5404a87d37ac253fa50c0839772ccde6745c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:134ee55063a0ce1e9ae80e14e7d4412d40320285f3e74dd116773ef49492047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fa70560d32c3309dd4f2ad8d06fc8381d9b8b61f718308e9c54ca5a212272d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:a306852d26bd49b91723c0384f8dbccd5332b32e891f026135de87f8b08678c0
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
$ docker pull docker@sha256:d681001b65c02149db1800056f3e8dd04c46ba0af7cb9c4d9aea4466b83dc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67634487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b8a9636b980903f8dedee7362d64da168948fe9de688eb1eb323b9af3c8773`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:c0a1bfd10bc1592a1a5bdb1188ff22e5c6a82e5bb369673c1f06e473fd04ffa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670bf0b3949291682be4fe1f8db801b2ae028f60dbb1657a4dedf8804aa2d85c`

```dockerfile
```

-	Layers:
	-	`sha256:1fb0079f2ad11a0540560cb6484f23edc1707fc7d87c4f30b45961b884f580dc`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:3230a03c4ca073df26ebbaba870d46bc674f8b2e32ba6d2f82f89a6f325ffcc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62881859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c059726e7ebd5080e0ca6f4218727b1d2e53686342e38bc27f96dd1168be019`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:956cbc52d49a237bd08951e7b9637f517528fc3326363ac6524657a16dc50c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbded9c7d487f194e8c3336ae42ac1c523ffe252aa26dd9fb31257198d84b0`

```dockerfile
```

-	Layers:
	-	`sha256:960aabcea856bd351dedf020ec8ddaa7c9413012e686f7603a12d7cc4a12d40a`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 38.1 KB (38107 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5eff9e2652593c1611264664a498725555be7f6ff83d2e06481b2122256bfe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61916265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de83e7723a53437758b6b2f1cb88adb5540488fe5c7b5890bb67cb0088247861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:1f2ea61961e414563265f4ba7c8d26f925684ae2644051145ceaf20e29c21f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b308c6f1b37816261ed8836666b71f7298aeeedba7790a3a230fa9e07f4fea`

```dockerfile
```

-	Layers:
	-	`sha256:2f81dc59dd0ec7406711323017f2226cad9b01517f4bac6e113cbd58f7caa9de`  
		Last Modified: Wed, 30 Oct 2024 01:02:01 GMT  
		Size: 38.1 KB (38108 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:154c7e471b3febf9fa66f77faa913357e19249b582ad27a0328d3646430f0aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63894469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c219c1d64de3adbc85c883284055b930aa729cd53ad11ceef3c601e814fd56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.3.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.3.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.3.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.3.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 17:04:16 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 29 Oct 2024 17:04:16 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 29 Oct 2024 17:04:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 17:04:16 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:04f0aae5aeb3b0a8dcf632384f22c0c32661dfb9be71fcec4502a8f9ff358d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78f90e01542faa4709016d39f5a2cd153e9bf893f752a51273713b146f6776`

```dockerfile
```

-	Layers:
	-	`sha256:8285d485a74cb3a9d489ff2efd03aa2e3411cb17a6cb42cbc927264a5820d076`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:d7f70287009a765ce9728d09ae0e1ef10ba2451ee7711298a3937da22dd1be5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:97316936aeccbcfae31c3ee8c744d6517a12ee5278ac04728221b7e239291fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b77c63afb3f34de27d291e46c605e0bd7afcd078b2e94c5d7e987b573ba2e79`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7c1b27cb672d81ee0e4513235c74e879beb8a1f41f90268f660474d36731c`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 981.6 KB (981576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81f22ddfe7fe47f5e6cc0d8b061586e9bfb03d6a0f9a72919fb92e33cd59ee`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ceb4b6852f66befe9b5f8c95412a41876132a80328dbdabbd31e81824ad0fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef05fd523513dfcd7ea96faec1283dcd08014ade10ca9180907f4dd5337c774b`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 21.3 MB (21303265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bc448d15ea248565c3b89094a50084e2f3eded7d9e10e06475223eb1af7a88`  
		Last Modified: Wed, 30 Oct 2024 00:47:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a071ebd27917f7d76a4782c16e2ee0c723cc0317334b4d40159700599dd079b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be0ed03e7637322aed785abe25aea41b8ebd0c9eac3dd6cd2682ea08d2d40a1`

```dockerfile
```

-	Layers:
	-	`sha256:ce55096dbabb40d46c9d04d1608c3f83e5f81604737859d3977b34896e8ae345`  
		Last Modified: Wed, 30 Oct 2024 00:47:47 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:df2018bf77ef9956bea679d229e86a0869408918e0c30acbc4557dd6f80054f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151462614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523b102871ed5328ab73a83b6c7007ebe05f5c35c50847019b01818de3303040`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f11fb7c9a7e46e95a9874adf87e8bafd06bb374be2c74d9ccb4622770585fb`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 MB (1023842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2211e328766d831433385aa9924c089cb0c332a4ed3171aacd3a97de972d5053`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f743305622d792bd249ad20ffdcebea86c516bb417c4a66762aaacc3f242638`  
		Last Modified: Wed, 30 Oct 2024 01:47:28 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73a168fb4569ec560dd604ca7e06e9a599446e1ebab8434667345f29399fbd6`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 23.2 MB (23155431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6318a4093bafc2dc1e678e46e5fd0d9b285777696e0d2be28d06cfe1521a5bdc`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:24d9a91db2e3210efb574de176582c85aecc21e44e45d2eaf780eb384d5f94ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f318787d6f843598fedc7cbfd1b4352e791d42d9506c520cc3af7c1cd448e45`

```dockerfile
```

-	Layers:
	-	`sha256:cb7f847a2eece9d610a02c1a0b9b474079c6f67184588b56f7f3dccbb52bf331`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:61b179d1c34a08d85d68df58fa90e4f8f6fe469f8e89aefb474d29f2e3bc8b97
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
$ docker pull docker@sha256:7ae4f4ed9ca65170b52d42bff92b6f5249f46d6a2adea790b295cbd11ed50001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134595725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c09412d256b557fc8d00ab4746daf8c3f70b708c4f46b8b799779dfbaad2c6`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:0a97babde3c5bfa6e0f381d265b92d73175f4d91df8936e543b54a5b5bd40d5c`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 7.9 MB (7889548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f756db54c005fafed2e65a9e16b724e915a4f82effe22525250a2f7335df1e1e`  
		Last Modified: Tue, 29 Oct 2024 22:58:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d52b0db9bd3b13cd3dc92676cf8cfcfcf1cdf619c1b1dc1a0e7b8c0b4a82d5a`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.6 MB (18563405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3782a90327cd2c7065cde1633d02ee995858d660cfcfa0ab8fb40e6fedceb681`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81f86317db7f55b57b37766542a7e6120fac463f72f221dee2d79081823dbf0`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 19.1 MB (19117853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d74d185c3414f83cfd80ff8c8e1b7844ba6414ea3943817b6d6b4a15b302c56`  
		Last Modified: Tue, 29 Oct 2024 22:58:22 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e0f0388bb59e28c83359d0d56d9d93393a9be936effbd746dacdac2dfb6145`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b30d9583353056f88049261b29309dd9739943b07594fe286e620330a8c960`  
		Last Modified: Tue, 29 Oct 2024 22:58:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234d1ea407ae90560f7955a9fb13b7533c2ea7890e77ad991fdd74c60dc9c51d`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 9.1 MB (9067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0efa79573e65394eb1fc7eab31f9879bd9aebfdd44a7ee364712f214dc7d5d0`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 89.2 KB (89230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28fdec5b4ff616320d65926db09bc4064cbc8589ec3bc6358472f60e08e632`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70cf11f47f8fea463c976ed419c6345871678226ad7ba910b4c8fb0110d70f3`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 57.8 MB (57798994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cce4b90e06e6a6e596cef8f6132ec92a700e25db647abbbb32adcadd69b270`  
		Last Modified: Tue, 29 Oct 2024 23:57:00 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacc6a426998b9fbb4d4ec8fdc20ee10f93e8539658e9307f8dff0e54a216d49`  
		Last Modified: Tue, 29 Oct 2024 23:56:59 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:ea1cb01ab25aef8bac57575dff1581c0ab0b7234a2c679b3cbbc63a37daa652b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a59f98823452ca98ae164aa1204ec20ad7e607f657a376a43cec16b155dac88`

```dockerfile
```

-	Layers:
	-	`sha256:3830566c3eaf5cc4dbbbd28d0f0299fde426ec5dea7574b5936dc0547698dfdc`  
		Last Modified: Tue, 29 Oct 2024 23:56:58 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:487648e68c72105ca605ef76314369f8b14dfed3deb0438ea0aff9edceaf6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125547369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a20354063382e69b1e8fb3b5daf83a3922ffba79e949a2efcab6ded41fb3ea`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552aacdff8580b684a379cb7bc30ea8c6c4f07bdbcc35e1ffb6274fdd9362f9a`  
		Last Modified: Wed, 30 Oct 2024 00:53:56 GMT  
		Size: 18.0 MB (17958867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fce6476e2914fc00a618a927807223cb257fc855f523fd96c3ae5baf6eab22`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606289d1c6032347cb1cc4d98936e018d302e77c639be287148d76f454f9732b`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05dfd27896c16a96b4d35ad28dcd8460225e8da0ca043b92b4cf4c731ab928e`  
		Last Modified: Wed, 30 Oct 2024 00:53:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1754d881ef4d4f68273b2edce345798a9aa23e158279c86d84dda4cfc0a1ab58`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 9.1 MB (9060270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00948692eb013888251aff8f84cb7621e4dca8405fcd07cd1d89175a7353f984`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 88.4 KB (88414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545e25370a464df6c7964012a1c272b2cd11e29e5a10b8904eeaed91e96cb023`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6a990fc7bd885d2bc9afaec8fce150d605ec106fc149699fcbdd0ef6764433`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 53.5 MB (53511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bf31bb5ccb5cbd048ecbca433b355799e2ef38257eac9f8d21f116de14fd0`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5643fedf0d759b03a9e52395b10f0a2a766f0bc3d082de19dcbc7ca876381f55`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:2cdc51915734f0194071545eeaaa26319cb39d3e0b7dd6d651fd6dcd14877941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d951851be1c2ee4e3f7e6cda922ccd984538cab46ba1da6d467952da68238590`

```dockerfile
```

-	Layers:
	-	`sha256:51f619804b1fae18230dbb309dd1b8487b741e53da3153937bd8f12f135f8764`  
		Last Modified: Wed, 30 Oct 2024 01:47:24 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:c97d9d465252d1ddbf9ef0c51faee757947f26681b21b8967c36d74c370c419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123745944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae666b144de6fbb7034bc5eb7c858a249334ff38f32be31e1af9d4abe476388`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7430f2b67e232672ddbb61b6ae9d43e06f622beb279905f20c4c95b064306be`  
		Last Modified: Wed, 30 Oct 2024 01:02:03 GMT  
		Size: 17.9 MB (17938776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad745cbd790e11d12b7d0f2de6c23555d68ad8ac6a7c7330118a3f6560458281`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e167e73ee0e58180a337811154ab3483ac61d6d59e8b7f0e5bb3efacbbb0f4`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47b7c573d595501edbb43feb393bd00ca668e6b217a3eabd76058ab390bccd5`  
		Last Modified: Wed, 30 Oct 2024 01:02:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a1497ea905d20cf7cab17b898d03bd904c5351694045a6ab3c7efcb88d82ef`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 8.2 MB (8228347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b567e73cea2c552731ca1b950499cc5900c99bd142fe68c57825a5bf5a0ed`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 84.5 KB (84501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1dabf0202b6475f99d0c28537dd49d7b353331c0fa104338d832044a30dbd3`  
		Last Modified: Wed, 30 Oct 2024 01:47:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc59a3ca7d72fd15357bb3b9f0bd14e6e5f07929c4578a30b08d599eb2066290`  
		Last Modified: Wed, 30 Oct 2024 01:47:29 GMT  
		Size: 53.5 MB (53511039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4d7fb1a1f19111877d85dddfd9bce3aa5c2cdbc29f6361a11c98e739cf4ee3`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318f28f45a5a4145e25dcc0da46a94f90500a3e54630c6727a4f93680d45401`  
		Last Modified: Wed, 30 Oct 2024 01:47:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:01ba94aa188a6e5e974c25d9a6c374e644d6f36c7727e84a22861286fd73b1b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0438809c7080b00b5ed4df5197f3b90c85a7e3610b5893a5e5a3668b36a9054`

```dockerfile
```

-	Layers:
	-	`sha256:778712a02fb8224719a857b6abc7b0d96728c593e5935de9b7d3863f4b9975fa`  
		Last Modified: Wed, 30 Oct 2024 01:47:25 GMT  
		Size: 34.8 KB (34771 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:d445603e6e21152a7e85aafb15d3d13cafd1e22e08ed886f46c758682e3408f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127281991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689cb25e0bf15f3b86128af134f458095277a5e531098614a6018f15b9f8e6cb`
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
ENV DOCKER_BUILDX_VERSION=0.17.1
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-amd64'; 			sha256='aa7a9778349e1a8ace685e4c51a1d33e7a9b0aa6925d1c625b09cb3800eba696'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v6'; 			sha256='8c287b02430036d42323052e228ee8e26a6e7f7c5858b170f6f82be812d8043b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm-v7'; 			sha256='5454c2feddb76000c22cb8abafe8f4a03e6fee12aae9031f9e02b661e76012c8'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-arm64'; 			sha256='de05dccd47932eb9fd6e63781ab29d2b0b2c834bbdd19b51d7ea452b1fe378d3'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-ppc64le'; 			sha256='29b4f2de5a1e6ecb4096868111d693a8ba4aaf144d535242ce19fc4154f94a4e'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-riscv64'; 			sha256='e67d26acb10c4529b9b5ca4e20781865d63e538228c566af6d1e91da65cdb992'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.linux-s390x'; 			sha256='9a3a4376025d1c2771ac69aceff0bcb19a2594413e318a34455af037ce903f06'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 20 Sep 2024 18:21:55 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Fri, 20 Sep 2024 18:21:55 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-x86_64'; 			sha256='1cddcb3399cc68c385796a6ab441ab5734d4c6a0cb4713bd2bf3f0d384550a38'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv6'; 			sha256='e8aa55c053feee38474d97150d908268b666915160a8e588ca2938350a3b7dee'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-armv7'; 			sha256='3dc0b1bea00ca66cd17cdc0200a9a2f7441d501598de58bb3621c5e04da7b1d3'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-aarch64'; 			sha256='06a8dee876dcae79c6b0923b73b16fcc12b003b05556533079b27e24306e88b9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-ppc64le'; 			sha256='2ba0a78a2c56576389c9ff6f8d501e8385c2ed99ec9634f852c668e56cf7487d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-riscv64'; 			sha256='8aa7eeff2e25561691e3a653913d7d2f5dd23791c7674967b1e0498f73f74c54'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-linux-s390x'; 			sha256='431425d29c149d21d67a4e5ddc9490dc92c256ef52f8034903481a3d848e410c'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
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
	-	`sha256:492591cc18739d2c6e5e3f0ea906c09f20e1449d89c137b2a6b0fcadb7580baf`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 8.0 MB (7997646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685c55f9b48c0be02c858da8e2dc5806ec18001acdc25ea71abe30c64aaa97a1`  
		Last Modified: Wed, 30 Oct 2024 00:02:29 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913f24e0e2cf8b2177858492bdd85a0572dea04b7b14adca53c83ac1897d375`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 17.5 MB (17513974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21424b25f29d93688bc263641b8d026f88c95aa07ff12ca1d8d9748ae3d310cd`  
		Last Modified: Wed, 30 Oct 2024 00:02:30 GMT  
		Size: 16.8 MB (16800777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe46ba0db371305074d3ea21cb11533d62539e76b6fdf7eaedf0402949df31`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 17.5 MB (17492273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4c3f9c609719c14cab3e07f1415383c0f02f4051eb42a203368d5bbf6138a`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0deed07b82b517c24c0a850023df344f731dd48be585097f28fead6016851ebd`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e02d49a171ba49cb964581e9267a02e7a85f890aee83a7c34d03dd53b2ea07f`  
		Last Modified: Wed, 30 Oct 2024 00:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64671d792402d3ea0d2ba6af5eaece9077f4b4b43f2868db03444411f6f863cc`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 9.9 MB (9854902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494b07e08a56e3a68396c7c305321f84f31325a37d6007aa9600defd4ca5b06d`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5baf953217fe0c9f7bb47fdb6ae56080005e879057ac60f786ebe0a97ec8af8`  
		Last Modified: Wed, 30 Oct 2024 00:47:43 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0d1a0ef5cb7272ab3384908af07426e0315a22b0b0d753a0ba6e4bd140bb8e`  
		Last Modified: Wed, 30 Oct 2024 00:47:45 GMT  
		Size: 53.4 MB (53428165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f7db68d83260a22e40cb7e8ac243ab91c0dd02fde76da23cb3962e9fa21fa`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 1.5 KB (1512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d6aa17065c91d9f96764290a67c1ead827d2c63b466aa43bc5bacb5c31b65`  
		Last Modified: Wed, 30 Oct 2024 00:47:44 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:f78e6d64bd81b49c04a54aaccab973c61c3472bba52960c84f2d3f8be8c96199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0421fb58c9f5f43861c81b7e4f1c89053bd2d68c123584538b03749676c03b`

```dockerfile
```

-	Layers:
	-	`sha256:4841a824c0bc2d08344d309f01c299fb69e27068f47b6e5be14223a55f0b0e70`  
		Last Modified: Wed, 30 Oct 2024 00:47:42 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:2b808b9cad9d1cf6d10e1b0098f5404a87d37ac253fa50c0839772ccde6745c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:134ee55063a0ce1e9ae80e14e7d4412d40320285f3e74dd116773ef49492047d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:c1245d2fd1732a957e8b50baad51ce75a49af9a9b890f7fa3e7b8a35e8221c4e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960434771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01ee495b8b3f60a93a92f51fb4c505b7aae848a227d1e8aa66ea15e18e63883`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:58:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:07 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:08 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 22:59:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:20 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 22:59:21 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 22:59:22 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 22:59:32 GMT
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
	-	`sha256:93a3ccf2066cd12a2e7cc953c8b331ff1bd5f983d714b90abf36a91c4bceab89`  
		Last Modified: Tue, 29 Oct 2024 22:59:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08b72822a5c3fe5e17b521c1c0430252680cd21284ac583d123c04eb5d29127`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 479.6 KB (479637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224b641fecc2d4c3e561107afcd7598706b16b9d0e4e8db4fcf36aaf6b5001a`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e7ef40b1518b7bc76a6cf4268c97390e27197e2f83a5e877c3d465834c6ce`  
		Last Modified: Tue, 29 Oct 2024 22:59:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efe54202b2a54f4a5bca39aa0e543f4f6d28f8d28585e7822e79ddcfe49a375`  
		Last Modified: Tue, 29 Oct 2024 22:59:42 GMT  
		Size: 18.9 MB (18876194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea04309fd9807ea0d89bf9df03ef3027b6c2378e90d4773bcb9c988435222b01`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2b2deae03f998def3d86e6a758df0996a4a2cf3448cec83ff6125904bd9f5a`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae70b9162235bd21c230d777b1714c5428e1a1d81d0868de98be4a8ed120251`  
		Last Modified: Tue, 29 Oct 2024 22:59:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038f29234f8974fd7c2d54c025936267203851a1bf9e64994f7219cf8d6dc12d`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 19.3 MB (19268304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512f40573fd8fbd5cb028fbd008a21492681711891ae5d8dcfc0fd36f4971c06`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe71b60652002b390520605e15f26368138101f7a887bb20098f4572de1ae3a`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d348d403c0515dab6fd6e77d3e44581c3ff253cf0d50aa453cb63b8d8a643c`  
		Last Modified: Tue, 29 Oct 2024 22:59:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d00cef146bb615c3157fff54a2a602acb779cbf5bb23a94fe32955dd566e72`  
		Last Modified: Tue, 29 Oct 2024 22:59:39 GMT  
		Size: 20.0 MB (19973675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fa70560d32c3309dd4f2ad8d06fc8381d9b8b61f718308e9c54ca5a212272d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:774a68613f0bfb59a7d502eaf0a687a0cf7de4dd1c45800f85b5deac8371289b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1857902556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5131a2a34f7784aceb18708cb997ae4df3734229a96ff58c050ff308300abc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 22:58:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:59:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 29 Oct 2024 22:59:33 GMT
ENV DOCKER_VERSION=27.3.1
# Tue, 29 Oct 2024 22:59:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Tue, 29 Oct 2024 22:59:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 29 Oct 2024 22:59:50 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 29 Oct 2024 22:59:51 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 29 Oct 2024 23:00:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 29 Oct 2024 23:00:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.0
# Tue, 29 Oct 2024 23:00:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.0/docker-compose-windows-x86_64.exe
# Tue, 29 Oct 2024 23:00:03 GMT
ENV DOCKER_COMPOSE_SHA256=07ed10572bed0c42e5477bd33f9eb8f1b1c640d83120cc59feb7ce28f0c1bf86
# Tue, 29 Oct 2024 23:00:13 GMT
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
	-	`sha256:8ac9abafc5bec837c1d9297342c76f4e12cf81ac11f8b5f4c28ca269a447dbb6`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f24f35b4d3e2f21fa6cdda9036708dd43b5176af33cdf534115bbd1d78dd413`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 490.8 KB (490790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241374395b6809ce27e3acdc37ad9fc65ccef418a928e7e19a1745953ca95adf`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d73da2e4c13940adb2e01d90c23924023ec518fd24a79ad0668165add72c0a`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5538e5702b1667f6ad1539e757291b95e43742d1d0699cb3fea9e2a74d015408`  
		Last Modified: Tue, 29 Oct 2024 23:00:23 GMT  
		Size: 18.9 MB (18851934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31e9c29f21f51a164adbe26241fd9bda699ba057a51da111554c4cb7411bc4`  
		Last Modified: Tue, 29 Oct 2024 23:00:20 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac7f971f1ae634d2730248b678e893ecb7c4bbf50b39d9564a3825cf0c9f4de`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368db46117b43533a07294de56ed15e86f2b9c12899209f95406b10f0e64d81f`  
		Last Modified: Tue, 29 Oct 2024 23:00:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de032694a3ec3ba5cb0b9772a73e382d994b01f0dc79a1e89e084d81ac22d10`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 19.2 MB (19246597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858f2174f2866716738c78eb1ce71c47ac6b51cf383336b160dc54ab799983ca`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e75c6ceeb8a39a48851d4dc76114c93f40f2e8d2b76551a868d5b081a878e5`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8fa03b10a706f95164407f2bcede9c9851f718de2b5ecece3f2358eee59b11`  
		Last Modified: Tue, 29 Oct 2024 23:00:18 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eac5a86f562df288c8b7d86d7a2f014953c1cb6fe2afa8c277d61176a0a751e`  
		Last Modified: Tue, 29 Oct 2024 23:00:21 GMT  
		Size: 20.0 MB (19959923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
