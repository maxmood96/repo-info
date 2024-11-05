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
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-cli`

```console
$ docker pull docker@sha256:ac6f46b675c07b6dcf4e1a89a516d0e68bcb1123bdd34357d372f930c3f18398
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
$ docker pull docker@sha256:eb336b23b3d240665e0275c8964f2b57017f22981f29afa45ccf2f475304b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62983016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc481427bf7e202f772ad0535d33ac3e25b00894384727f5cd1df14dcc60f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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

### `docker:27-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e12bc150120212cffb0a839f2b1ff4c9fa62369a95dd1a5338438033e3cf770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528fc1ca268e05da5a51429f7fe0033d9661f857d0f03fc785fcb62f23f310a1`

```dockerfile
```

-	Layers:
	-	`sha256:458ae9a1d14ca6fff3eb81fed46ea496e71c73f18f947f756e70e29526724da9`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
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
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:dd77a9a919b6a1705a2a17166c04bc4f8b151cad6b2ccdffbdcdb08f7be4352a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2dd57cbf29dd658257b6c3eeb1a230eaefd0794138639f6661b9e11669709ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefbcd051f4edc3bf817c4e1b764f49b77fedacc2eab0d86a474367f637cd651`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de2f8aeefae8f521965b645b578c2e7a29c76ed6169962d672fe4da6d1bf600`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 981.6 KB (981574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82ff44cdf375f153ebdc935f6cae5e20ffae2e9575f279f60e69d01b9c5a078`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9e8b106d2c7fd193d15bfab73e33edbfc6302d5fc2fc1d8eb70142a00c3a9`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5451bc9f4d02b819e39e925e4ac181652709fc644bb338ef7e817c41bcced57`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 21.3 MB (21303258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80215e28ed17b6bf9d6a52b09981a23d2b65280dc741a34687f21caa6f7fe85f`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:22cebf84d1e63d365a53b3878304b4a7436ade5da185d10efb4b3d70a3fd9829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb797491f1ddfe1258accc6d2799e2e6e41e019eea499c92bf0f623022ec7360`

```dockerfile
```

-	Layers:
	-	`sha256:bbdb439fe5cb43ed576e4cbebca2a54ea0947fbaf0821424c3c0dbe8da53583e`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78052ae2fc3bcf30217493a52fa2b14afbdc85d439848458c7203ef5a31fb8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151463056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caee4d5cb393a69d5b13c5395d2389284bea4183760717bf11a03c11d6aa55d8`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbfb0c4576bb6900da94921e688a351783084d76ab5e87b93a3968b5c80ec5`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 MB (1023837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89f947555fbe3ca9d2709c3f42f9ae60e0cd83474b404aff357c18a3e7aeb1`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494570759f6fabda91082b6b23ecaa807c71ff431e2edc30d971f0d22ca494cc`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6d1734c3a044687550d5c13db259612d42dd9f367c0b4f39d713717576a22`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3a1425de8fb899f5aac1bf596a775e5337ee4b29e9536b5c8e42c415fc200`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:35a24cd2aaa8bc23c10efc235014616b1a6a9ddefdb9d3e711aedbd5dc10f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0755b69e9c2eb482d83b796194fce0941044f76e0bf3aae5e6cbb72f6077f0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6796f77181c3c4c8d5b0f5b8d79cda852662ac2408c12a95c12a2504b6d11f`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:9920491f2ef7ea58eb44b9081c71f6b0b377e156429480e162d2da1a35709c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-1809`

```console
$ docker pull docker@sha256:abaeaa13d6e4a1dc3e6c6fc8daf40f6277234856a531dfb642a7cb7e62c9cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:27379678fb59e194cd712ebb0e1c2815c075f491a692d84c185f9c023d3e6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3`

```console
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-cli`

```console
$ docker pull docker@sha256:ac6f46b675c07b6dcf4e1a89a516d0e68bcb1123bdd34357d372f930c3f18398
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
$ docker pull docker@sha256:eb336b23b3d240665e0275c8964f2b57017f22981f29afa45ccf2f475304b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62983016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc481427bf7e202f772ad0535d33ac3e25b00894384727f5cd1df14dcc60f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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

### `docker:27.3-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e12bc150120212cffb0a839f2b1ff4c9fa62369a95dd1a5338438033e3cf770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528fc1ca268e05da5a51429f7fe0033d9661f857d0f03fc785fcb62f23f310a1`

```dockerfile
```

-	Layers:
	-	`sha256:458ae9a1d14ca6fff3eb81fed46ea496e71c73f18f947f756e70e29526724da9`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
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
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-dind-rootless`

```console
$ docker pull docker@sha256:dd77a9a919b6a1705a2a17166c04bc4f8b151cad6b2ccdffbdcdb08f7be4352a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2dd57cbf29dd658257b6c3eeb1a230eaefd0794138639f6661b9e11669709ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefbcd051f4edc3bf817c4e1b764f49b77fedacc2eab0d86a474367f637cd651`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de2f8aeefae8f521965b645b578c2e7a29c76ed6169962d672fe4da6d1bf600`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 981.6 KB (981574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82ff44cdf375f153ebdc935f6cae5e20ffae2e9575f279f60e69d01b9c5a078`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9e8b106d2c7fd193d15bfab73e33edbfc6302d5fc2fc1d8eb70142a00c3a9`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5451bc9f4d02b819e39e925e4ac181652709fc644bb338ef7e817c41bcced57`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 21.3 MB (21303258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80215e28ed17b6bf9d6a52b09981a23d2b65280dc741a34687f21caa6f7fe85f`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:22cebf84d1e63d365a53b3878304b4a7436ade5da185d10efb4b3d70a3fd9829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb797491f1ddfe1258accc6d2799e2e6e41e019eea499c92bf0f623022ec7360`

```dockerfile
```

-	Layers:
	-	`sha256:bbdb439fe5cb43ed576e4cbebca2a54ea0947fbaf0821424c3c0dbe8da53583e`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78052ae2fc3bcf30217493a52fa2b14afbdc85d439848458c7203ef5a31fb8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151463056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caee4d5cb393a69d5b13c5395d2389284bea4183760717bf11a03c11d6aa55d8`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbfb0c4576bb6900da94921e688a351783084d76ab5e87b93a3968b5c80ec5`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 MB (1023837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89f947555fbe3ca9d2709c3f42f9ae60e0cd83474b404aff357c18a3e7aeb1`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494570759f6fabda91082b6b23ecaa807c71ff431e2edc30d971f0d22ca494cc`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6d1734c3a044687550d5c13db259612d42dd9f367c0b4f39d713717576a22`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3a1425de8fb899f5aac1bf596a775e5337ee4b29e9536b5c8e42c415fc200`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:35a24cd2aaa8bc23c10efc235014616b1a6a9ddefdb9d3e711aedbd5dc10f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0755b69e9c2eb482d83b796194fce0941044f76e0bf3aae5e6cbb72f6077f0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6796f77181c3c4c8d5b0f5b8d79cda852662ac2408c12a95c12a2504b6d11f`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3-windowsservercore`

```console
$ docker pull docker@sha256:9920491f2ef7ea58eb44b9081c71f6b0b377e156429480e162d2da1a35709c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-1809`

```console
$ docker pull docker@sha256:abaeaa13d6e4a1dc3e6c6fc8daf40f6277234856a531dfb642a7cb7e62c9cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:27379678fb59e194cd712ebb0e1c2815c075f491a692d84c185f9c023d3e6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1`

```console
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-alpine3.20`

```console
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-cli`

```console
$ docker pull docker@sha256:ac6f46b675c07b6dcf4e1a89a516d0e68bcb1123bdd34357d372f930c3f18398
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
$ docker pull docker@sha256:eb336b23b3d240665e0275c8964f2b57017f22981f29afa45ccf2f475304b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62983016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc481427bf7e202f772ad0535d33ac3e25b00894384727f5cd1df14dcc60f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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

### `docker:27.3.1-cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e12bc150120212cffb0a839f2b1ff4c9fa62369a95dd1a5338438033e3cf770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528fc1ca268e05da5a51429f7fe0033d9661f857d0f03fc785fcb62f23f310a1`

```dockerfile
```

-	Layers:
	-	`sha256:458ae9a1d14ca6fff3eb81fed46ea496e71c73f18f947f756e70e29526724da9`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
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
$ docker pull docker@sha256:ac6f46b675c07b6dcf4e1a89a516d0e68bcb1123bdd34357d372f930c3f18398
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
$ docker pull docker@sha256:eb336b23b3d240665e0275c8964f2b57017f22981f29afa45ccf2f475304b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62983016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc481427bf7e202f772ad0535d33ac3e25b00894384727f5cd1df14dcc60f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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

### `docker:27.3.1-cli-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:6e12bc150120212cffb0a839f2b1ff4c9fa62369a95dd1a5338438033e3cf770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528fc1ca268e05da5a51429f7fe0033d9661f857d0f03fc785fcb62f23f310a1`

```dockerfile
```

-	Layers:
	-	`sha256:458ae9a1d14ca6fff3eb81fed46ea496e71c73f18f947f756e70e29526724da9`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
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
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-alpine3.20`

```console
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-alpine3.20` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-dind-rootless`

```console
$ docker pull docker@sha256:dd77a9a919b6a1705a2a17166c04bc4f8b151cad6b2ccdffbdcdb08f7be4352a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27.3.1-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2dd57cbf29dd658257b6c3eeb1a230eaefd0794138639f6661b9e11669709ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefbcd051f4edc3bf817c4e1b764f49b77fedacc2eab0d86a474367f637cd651`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de2f8aeefae8f521965b645b578c2e7a29c76ed6169962d672fe4da6d1bf600`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 981.6 KB (981574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82ff44cdf375f153ebdc935f6cae5e20ffae2e9575f279f60e69d01b9c5a078`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9e8b106d2c7fd193d15bfab73e33edbfc6302d5fc2fc1d8eb70142a00c3a9`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5451bc9f4d02b819e39e925e4ac181652709fc644bb338ef7e817c41bcced57`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 21.3 MB (21303258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80215e28ed17b6bf9d6a52b09981a23d2b65280dc741a34687f21caa6f7fe85f`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:22cebf84d1e63d365a53b3878304b4a7436ade5da185d10efb4b3d70a3fd9829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb797491f1ddfe1258accc6d2799e2e6e41e019eea499c92bf0f623022ec7360`

```dockerfile
```

-	Layers:
	-	`sha256:bbdb439fe5cb43ed576e4cbebca2a54ea0947fbaf0821424c3c0dbe8da53583e`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27.3.1-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78052ae2fc3bcf30217493a52fa2b14afbdc85d439848458c7203ef5a31fb8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151463056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caee4d5cb393a69d5b13c5395d2389284bea4183760717bf11a03c11d6aa55d8`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbfb0c4576bb6900da94921e688a351783084d76ab5e87b93a3968b5c80ec5`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 MB (1023837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89f947555fbe3ca9d2709c3f42f9ae60e0cd83474b404aff357c18a3e7aeb1`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494570759f6fabda91082b6b23ecaa807c71ff431e2edc30d971f0d22ca494cc`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6d1734c3a044687550d5c13db259612d42dd9f367c0b4f39d713717576a22`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3a1425de8fb899f5aac1bf596a775e5337ee4b29e9536b5c8e42c415fc200`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27.3.1-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:35a24cd2aaa8bc23c10efc235014616b1a6a9ddefdb9d3e711aedbd5dc10f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0755b69e9c2eb482d83b796194fce0941044f76e0bf3aae5e6cbb72f6077f0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6796f77181c3c4c8d5b0f5b8d79cda852662ac2408c12a95c12a2504b6d11f`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:27.3.1-windowsservercore`

```console
$ docker pull docker@sha256:9920491f2ef7ea58eb44b9081c71f6b0b377e156429480e162d2da1a35709c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27.3.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-1809`

```console
$ docker pull docker@sha256:abaeaa13d6e4a1dc3e6c6fc8daf40f6277234856a531dfb642a7cb7e62c9cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:27.3.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:27.3.1-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:27379678fb59e194cd712ebb0e1c2815c075f491a692d84c185f9c023d3e6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:27.3.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:cli`

```console
$ docker pull docker@sha256:ac6f46b675c07b6dcf4e1a89a516d0e68bcb1123bdd34357d372f930c3f18398
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
$ docker pull docker@sha256:eb336b23b3d240665e0275c8964f2b57017f22981f29afa45ccf2f475304b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (62983016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74dc481427bf7e202f772ad0535d33ac3e25b00894384727f5cd1df14dcc60f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
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

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:6e12bc150120212cffb0a839f2b1ff4c9fa62369a95dd1a5338438033e3cf770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528fc1ca268e05da5a51429f7fe0033d9661f857d0f03fc785fcb62f23f310a1`

```dockerfile
```

-	Layers:
	-	`sha256:458ae9a1d14ca6fff3eb81fed46ea496e71c73f18f947f756e70e29526724da9`  
		Last Modified: Mon, 04 Nov 2024 22:03:33 GMT  
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
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:dind-rootless`

```console
$ docker pull docker@sha256:dd77a9a919b6a1705a2a17166c04bc4f8b151cad6b2ccdffbdcdb08f7be4352a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:2dd57cbf29dd658257b6c3eeb1a230eaefd0794138639f6661b9e11669709ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156881143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefbcd051f4edc3bf817c4e1b764f49b77fedacc2eab0d86a474367f637cd651`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de2f8aeefae8f521965b645b578c2e7a29c76ed6169962d672fe4da6d1bf600`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 981.6 KB (981574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82ff44cdf375f153ebdc935f6cae5e20ffae2e9575f279f60e69d01b9c5a078`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9e8b106d2c7fd193d15bfab73e33edbfc6302d5fc2fc1d8eb70142a00c3a9`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5451bc9f4d02b819e39e925e4ac181652709fc644bb338ef7e817c41bcced57`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 21.3 MB (21303258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80215e28ed17b6bf9d6a52b09981a23d2b65280dc741a34687f21caa6f7fe85f`  
		Last Modified: Wed, 30 Oct 2024 19:48:33 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:22cebf84d1e63d365a53b3878304b4a7436ade5da185d10efb4b3d70a3fd9829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb797491f1ddfe1258accc6d2799e2e6e41e019eea499c92bf0f623022ec7360`

```dockerfile
```

-	Layers:
	-	`sha256:bbdb439fe5cb43ed576e4cbebca2a54ea0947fbaf0821424c3c0dbe8da53583e`  
		Last Modified: Wed, 30 Oct 2024 19:48:32 GMT  
		Size: 30.6 KB (30618 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:78052ae2fc3bcf30217493a52fa2b14afbdc85d439848458c7203ef5a31fb8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151463056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caee4d5cb393a69d5b13c5395d2389284bea4183760717bf11a03c11d6aa55d8`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbfb0c4576bb6900da94921e688a351783084d76ab5e87b93a3968b5c80ec5`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 MB (1023837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d89f947555fbe3ca9d2709c3f42f9ae60e0cd83474b404aff357c18a3e7aeb1`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494570759f6fabda91082b6b23ecaa807c71ff431e2edc30d971f0d22ca494cc`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6d1734c3a044687550d5c13db259612d42dd9f367c0b4f39d713717576a22`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 23.2 MB (23155444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3a1425de8fb899f5aac1bf596a775e5337ee4b29e9536b5c8e42c415fc200`  
		Last Modified: Wed, 30 Oct 2024 20:47:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:35a24cd2aaa8bc23c10efc235014616b1a6a9ddefdb9d3e711aedbd5dc10f958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0755b69e9c2eb482d83b796194fce0941044f76e0bf3aae5e6cbb72f6077f0`

```dockerfile
```

-	Layers:
	-	`sha256:3b6796f77181c3c4c8d5b0f5b8d79cda852662ac2408c12a95c12a2504b6d11f`  
		Last Modified: Wed, 30 Oct 2024 20:47:55 GMT  
		Size: 30.8 KB (30823 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:latest`

```console
$ docker pull docker@sha256:bda6cf6ae93dd0e40089a03e8215fbb9f4ddf0e344b7c577a484ebdaa34adceb
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
$ docker pull docker@sha256:c9ef42d5813a188f286e6552de3552a307c677a77190d8ee91951c753a5f8f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134594957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1bb32aa4e4e8d0a27dad96de9c0031047bf097564f7bd6d749157402b37dd3`
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
	-	`sha256:1059c1e97ec1cd37b1d5952a796a757b0268262b1085c0f3b1eb5eee20ff0c98`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 7.9 MB (7889569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4626f08e1c5ced4ec434552a580ad851273aa822a279f9f05cf8337d95ea0b`  
		Last Modified: Wed, 30 Oct 2024 18:44:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585b48cd25ed0a85df20887064426771344a1f7d89c0d48865d55818fd7ca7c`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.6 MB (18563416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1ff3ebc6e5513189529f7b5d7da4dfbf8e5521253a465f8c81b571c62de0ca`  
		Last Modified: Wed, 30 Oct 2024 18:44:24 GMT  
		Size: 18.4 MB (18437720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c590937406fb71f96f22707a4ed23f8edb380cd0f2319b42d5d113957f55f662`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 19.1 MB (19117094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de070b1506a38cbda04ae2aa7c5074bcab4feb89803dca598da6b109ff2e161`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d5a74bb977bd7441f38c228b97b9c63e07a2d87691c372a53c0c896306d4c3`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c3aad616a7f8caf6ace5ee121bac363b9eccba15339f30365bc220737363d`  
		Last Modified: Wed, 30 Oct 2024 18:44:25 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255b24bb69975603c97cd4fb78a16af56c862a340187a23bb3ec77b69b3ef97`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 9.1 MB (9067225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79148a297dd6fb20a448a8e0af7f2a2d203ddfeb741e5848263d30291ed5c0b5`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 89.2 KB (89231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b5699d3d52d317583d721591b305cbb5b0f67932b4fc8dad6743abcd24f2d`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500355c15e356aa1d6e4c1ea6b30dd624e19a8930e2c6c687e2210d8d91a8d7a`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 57.8 MB (57798948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc91948190ab19f2986af03349d0f87e4a50f5ebbbc42db6afa3c7dc7383e8cf`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8502a1ad17a13b6215b65ab92b989e5d9acca14654070fb652f7c186732c322`  
		Last Modified: Wed, 30 Oct 2024 19:00:21 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:a085e443ccd4d10418e4ad7d10b2fbf8abafefd54cacd9a8db44e059c6e3619a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 KB (34554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca5a2aa1697db96fb2b3e029d70ccb5a0d020619b69343fa4d949688f2ac285`

```dockerfile
```

-	Layers:
	-	`sha256:b84c26d1efd26e8efc784d9c4ad970f2618d4926a660e6f20bbdd664ca6d5ea3`  
		Last Modified: Wed, 30 Oct 2024 19:00:20 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v6

```console
$ docker pull docker@sha256:e99e6adfd1d81b173bb2f99ac1c0d0775bb17dbbaace7f51253d6114157c594b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125548192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d919c5c917e125165959ba8ade32d4c71ae753b544a4793893a5af1a06121c6c`
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
	-	`sha256:fa48222292e063b8b30731e162b9b8c783dc846652aa2eef0732db6671d0adb2`  
		Last Modified: Fri, 20 Sep 2024 19:56:33 GMT  
		Size: 17.1 MB (17145012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff65a1a41eeb4563c703da9df32ffde2d094c0ae65f82d2bcb7cf0356cb5044`  
		Last Modified: Wed, 30 Oct 2024 18:00:08 GMT  
		Size: 18.0 MB (17959761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab934ba2ae656f2d2940efa56165da37f05e243c1e83ca803e8de17973d003`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7148bd9d1e03160c3b2a1345fc3b1226245e9aba5fcae314396269c10e8d05c`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa2aed80a613f5df144510ecbb05b4dd3aab51c62a2444a213a0c1022e3534d`  
		Last Modified: Wed, 30 Oct 2024 18:00:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c286c468459776f5778211375a5afb97fabc02da864451a84e464f021297fa`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 9.1 MB (9060210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d315bd72fb4cbe82707ab9949065a1b4def42e868d605bbb7866a38a91427db`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 88.4 KB (88400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc6a083d53d793d8875ccfa56da0ac15d0547e1a0f6d6d65dc7e1abfaefa9f7`  
		Last Modified: Wed, 30 Oct 2024 19:00:03 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28a542bf03812083d553d64cb6368b4a67fe13937557da385af2a6ca278e32d`  
		Last Modified: Wed, 30 Oct 2024 19:00:06 GMT  
		Size: 53.5 MB (53511023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e447547f7ece1b3cfbc139ea3547c8ca080321b3d8d87b2d882fe77e5082f9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7a135f6b9a091d447f8a52f5b4ae4d1e622dcc1a05c9ba21404a0707a770a9`  
		Last Modified: Wed, 30 Oct 2024 19:00:04 GMT  
		Size: 3.3 KB (3265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:bbacdc92964a6ff89dbe21288e66f9908fb0f417521e06681922cd1a0d213300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd76a8ac7364f3054311bb8f1f964dad5d7206549d52df20326c2d7b8792c6a4`

```dockerfile
```

-	Layers:
	-	`sha256:8e025fa4e6566187b0e88049e95e847533e4010e4ff184cfc0dd1b3beb7a9c92`  
		Last Modified: Wed, 30 Oct 2024 19:00:02 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm variant v7

```console
$ docker pull docker@sha256:f3522fd1ecf3d22e444ab3e5262f2ee04b5a7b60005d67c24f7b8f4d25159f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123746297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddfbb209dc74576942314269b24180ecacd806064c3cdd343baae764c174cab`
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
	-	`sha256:efcdb11680d22fc4cfb594e812d1d29dd0048ef8c1b1c20a61f7f8c4bbb6b3b0`  
		Last Modified: Wed, 30 Oct 2024 01:02:02 GMT  
		Size: 17.1 MB (17135181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbfcbb8839fbfd6fdb568cb769e6f6260bb2b51da3add7c8243f21fa9365ae5`  
		Last Modified: Wed, 30 Oct 2024 18:00:05 GMT  
		Size: 17.9 MB (17939171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657c8762285139ce86e75531f7d61b224ab645645166fe0a0068e8df2d91e6fa`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abb36e8c6823af1e364b99044bfd3e4bc8cf75477c04a886e7ab89610c6aa71`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1001d4fb539565f10104ba8e77f9b51f8920384869e943c64a4cb459906eeeb0`  
		Last Modified: Wed, 30 Oct 2024 18:00:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec6852bf5f0985a62aad961750918c88d3fd5a368992bfc99adabe8f373237c`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 8.2 MB (8228293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26284960dec5e87e4f5e6c8151792898cd188cbdf3991ccaab5e150c475b31`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 84.5 KB (84505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3532f3d7aa3923e1f327ec6c1e7350ef194b4e295dfc1497b678f401043e7a`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98210ccbd8bb35c391921ab79e3cd8802a2057e1090db2826383df6d91f3fad3`  
		Last Modified: Wed, 30 Oct 2024 19:20:38 GMT  
		Size: 53.5 MB (53511038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f93c5af7ce074747b1cce1cbe5aaefe89b50567766f7e82717aa9c5905bee`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da47fcff66baecc1c2e3ceaacb578652b393ae2e70d0ec8e01e550df754df5`  
		Last Modified: Wed, 30 Oct 2024 19:20:37 GMT  
		Size: 3.3 KB (3262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:78d241972c2f8ea75a9da2c911bc1f55f144d46247d399059ddeccf459b1daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d3d80cf3ff4950d5c4325277ce21f8d73984bd647a472733117a69cc387d15`

```dockerfile
```

-	Layers:
	-	`sha256:4c8ded715513a0d5bc0ce8c5981685ca56065a71af67ae363c8a8b4fe1c9b55d`  
		Last Modified: Wed, 30 Oct 2024 19:20:36 GMT  
		Size: 34.8 KB (34772 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:latest` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:258f5961fba302c24d5e135c179589a4adaa25e0d183dc26557bf1ed4c1c08d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127282424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88ba78fab5d7f9bdbe6cf0bb97f568830f0d82192631127349760668a3c300c`
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
	-	`sha256:487c3979ccf4f6c88df3fe8a2bdc1bbbf5f8d4a99c2857967f12b270e7f9c716`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 8.0 MB (7997643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f34923eb05dcfac804ecaf82111e30facd941f9e985f0cdd639e6d1909d11d`  
		Last Modified: Wed, 30 Oct 2024 18:01:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd21c7e27087744c64d71960741c1d9b2066cfa51719438ca102d413f79cbb4`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 17.5 MB (17513985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945dc97825fe2b109d3a6e568768a5dafaf0961f79e4547eb359f5f4ffa57c4c`  
		Last Modified: Wed, 30 Oct 2024 18:01:50 GMT  
		Size: 16.8 MB (16800774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca4efbe384547b50b90381d33bbba0edc4234fe44e33cb5a51509cc9c4d027`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 17.5 MB (17492700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cbdde151491b41be764b3c7742d816f459b64d2e1ad893a0ab8ebbd3fb05bc`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1658cdb8c144dbe136886ed8bb17590334f438d8c0326504859e813fb489b8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc675deadb606ac8d391c6afd8655be6247f20eb009a6e3840b7d3b10edb03a8`  
		Last Modified: Wed, 30 Oct 2024 18:01:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0322f79b21730cf6c18d7cb8374e801d7fdc4a91f4549ad1996267592b912148`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 9.9 MB (9854898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51bd8615470c5f97fc0b56b61bc3b381c678e18487c52246cc74381861cb99f`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 98.7 KB (98662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c939871e895365823497893aad2b601be21976bdac27b57630c96c60e7ee72`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a39e24b4c96c2c7a7242daca9e20abf0827ce1d0f3bbe2f9f0dcdf1f9bcccc1`  
		Last Modified: Wed, 30 Oct 2024 20:03:05 GMT  
		Size: 53.4 MB (53428167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850d10af7131f9a8782c9867eaa8dffe8445e16c589be7a7e861cc27a4ca631`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcca2e6773e36771d29b9ed0c855b4aa24fe57e0bed4680c6892c62c4588909`  
		Last Modified: Wed, 30 Oct 2024 20:03:04 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:latest` - unknown; unknown

```console
$ docker pull docker@sha256:d7e48e772aaa22d7f8809e081f79eb4768f1bf856e309a5c1adacdcd49bee7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 KB (34832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888750ab39308135b1390f970fc74339ca648fc1ad4db435f07137e52f3c5fe6`

```dockerfile
```

-	Layers:
	-	`sha256:0c5b49b3644bc005ae429fe65f442ddafee35bda6effc410ffbf25019ed3fd30`  
		Last Modified: Wed, 30 Oct 2024 20:03:03 GMT  
		Size: 34.8 KB (34832 bytes)  
		MIME: application/vnd.in-toto+json

## `docker:windowsservercore`

```console
$ docker pull docker@sha256:9920491f2ef7ea58eb44b9081c71f6b0b377e156429480e162d2da1a35709c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:abaeaa13d6e4a1dc3e6c6fc8daf40f6277234856a531dfb642a7cb7e62c9cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
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
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:27379678fb59e194cd712ebb0e1c2815c075f491a692d84c185f9c023d3e6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
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
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
