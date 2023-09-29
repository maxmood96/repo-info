## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:fbc42b5c40d5b381777728a79e3191e9add2296ebf762899c50f42f41192a360
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:979ea05447c66ec192bd9473a5df008bc32a97125f171f6a349d64a1f23c3351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140557623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83b2ab08eb145bb43c027b35c643f8a9fe30127c973cbc3f0817ac72fa6f20a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 23:04:32 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_VERSION=24.0.6
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.22.0
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-x86_64'; 			sha256='e849450f1c5c20123aa7d63291e2a818b7a117f2e03e432853ece463dd09e67a'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-armv6'; 			sha256='46cabb4363c5fa66e63c6055b1d0a6fe2c7995350e48f14816a752ae4132231d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-armv7'; 			sha256='1a0d500eaae3c4ddbfdeb566896207c0628a671065b95d0e8907bca58f91d312'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-aarch64'; 			sha256='572a22000d408fb524258b379bf272a007c8da977c3e8d47c34f4e45dd7b1932'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-ppc64le'; 			sha256='4d1a3e89fdb7641422dc5cbcab48fd2da337b03265cb5ac2858c3425bacf952c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-riscv64'; 			sha256='c45193b98c54e5a898e6b9095f70b0487599f19ce25b579ed2fcc3f868415aff'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-s390x'; 			sha256='716aded74df512728638f1fe53170c46d94c1a085bc5a24108ce7101bc37bd81'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD []
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
USER rootless
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a3b84f9d8d423361dc29f5318ddebd6822e36fda6a7311f9552a63cb8eef92`  
		Last Modified: Thu, 28 Sep 2023 22:50:45 GMT  
		Size: 2.0 MB (2014281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e55f70a486915794c20cc8069b18eda66ec3ad4fc3e393361ae99e88ba75ac0`  
		Last Modified: Thu, 28 Sep 2023 22:50:46 GMT  
		Size: 16.4 MB (16390432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cde11686b6fc659bd672ba8ce623ac5ca01c69d8218e39dd606badef1de7a0e`  
		Last Modified: Thu, 28 Sep 2023 22:50:46 GMT  
		Size: 17.5 MB (17459269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c4cc17db7f3f57c0bae50e5fd393fd68e38699f03a6c066c4d4604eecc4332`  
		Last Modified: Thu, 28 Sep 2023 22:50:47 GMT  
		Size: 17.8 MB (17828705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e17aa0ca7f5f6173dbfade7886bf9acbc865d4ffb9a38208147d177035d17f`  
		Last Modified: Thu, 28 Sep 2023 22:50:46 GMT  
		Size: 541.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e17f377b828e4d21a41243d3d9f4dde9f454449e6b60f6101fa80a8eb8f15d`  
		Last Modified: Thu, 28 Sep 2023 22:50:47 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdee13b2421d9f03b8fbd0e7c1446672777969c9355275da3c606fb3819ebe30`  
		Last Modified: Thu, 28 Sep 2023 22:50:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4101e3fd4622702cd6fd8400c297646c55a0cca6cdf3c00b55e39ac12cb4313f`  
		Last Modified: Thu, 28 Sep 2023 23:57:21 GMT  
		Size: 7.1 MB (7080468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27f630a38f0e6d85aedd015d883fd254c7a64f9dd009b7fd72ca4b631f7657c`  
		Last Modified: Thu, 28 Sep 2023 23:57:19 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c9ea925f0c5f8bba8a5593154c3e1d5a84b186439a52a24d8a2503edec7f42`  
		Last Modified: Thu, 28 Sep 2023 23:57:24 GMT  
		Size: 54.4 MB (54351586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28d517cb2ce3b622fa933eb1572b6c818682ddc9562a1beac3909c27025bf08`  
		Last Modified: Thu, 28 Sep 2023 23:57:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a069f3d343dd4bffb49f0596ee0044a76162a48a148e84cca8fd10110d0da38e`  
		Last Modified: Thu, 28 Sep 2023 23:57:20 GMT  
		Size: 2.8 KB (2787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0afc29227d8cf51082dbbf7cf5d33b621a96ce202be330d51c96ce4a31f3b4`  
		Last Modified: Fri, 29 Sep 2023 00:56:09 GMT  
		Size: 1.4 MB (1362150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62e599cf58f63e80c987055ed41161f1b8b68720120a9d3e103e6f7fb1de58a`  
		Last Modified: Fri, 29 Sep 2023 00:56:09 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8e9a7a81fb42edf534149f3f86c1c04bf1935b0cbe7ef346acfdec66346fd2`  
		Last Modified: Fri, 29 Sep 2023 00:56:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cfb88dca21d17c684a40a1e5d6700eab5b9dbf8917850836335653460cb40a`  
		Last Modified: Fri, 29 Sep 2023 00:56:11 GMT  
		Size: 20.7 MB (20660316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39be0185f7d48a2e786443b48e601e25c789003b10244aee2090a5ca200fe5c`  
		Last Modified: Fri, 29 Sep 2023 00:56:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:88364d3a5bb21f498b5904e30b80a1fb616ce511dabc259340695912dea08150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.1 KB (776089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fa1df5be10b90384ff5c7bc5a7119e9ef2f9dff9ab67ebf886f158328f0499`

```dockerfile
```

-	Layers:
	-	`sha256:557394f9405b11ea1c13385caf6f3eb70085d8ca2e4662d89e74adf4a9b557b5`  
		Last Modified: Fri, 29 Sep 2023 00:56:08 GMT  
		Size: 745.0 KB (745005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b2b2e04bb1b13008d70ba9e12e508bda7282b41ad0566bc765270252f010e7`  
		Last Modified: Fri, 29 Sep 2023 00:56:08 GMT  
		Size: 31.1 KB (31084 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:7dd6a133785619db1d964124d800d7100c1e9be8c27e424e542f045037d0e30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133697571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e716d38e4507b77ec6bf6f62901d97405cb6947767752296565d654c830bea05`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Tue, 05 Sep 2023 23:04:32 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_VERSION=24.0.6
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-amd64'; 			sha256='311568ee69715abc46163fd688e56c77ab0144ff32e116d0f293bfc3470e75b7'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v6'; 			sha256='c1bab0c7374406d5069f60b291971d71161fbd3c00e8a8fb1b68b9053eda8a4e'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm-v7'; 			sha256='4defdf463ca2516d3f58fef69a6f78cbbb8baf16d936cdfc54df4a4be0d48f7f'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-arm64'; 			sha256='565e36085a35bba5104f37365ba796c111338eea1a0902b3a7ff42e2e1248815'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-ppc64le'; 			sha256='c5f5cb9957890873a537c7ff5c4eef36132339622baeabb37a4b9b7251ddf836'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-riscv64'; 			sha256='c0adc4b4625f7e3df7dcdec840568f918673f2ed4bcd03ca1e63ea2a5627ca35'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.linux-s390x'; 			sha256='02916c76c3872fd0b3fa57e71403fee92b6be10f350b96a5ff99e7914dd277b8'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.22.0
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-x86_64'; 			sha256='e849450f1c5c20123aa7d63291e2a818b7a117f2e03e432853ece463dd09e67a'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-armv6'; 			sha256='46cabb4363c5fa66e63c6055b1d0a6fe2c7995350e48f14816a752ae4132231d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-armv7'; 			sha256='1a0d500eaae3c4ddbfdeb566896207c0628a671065b95d0e8907bca58f91d312'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-aarch64'; 			sha256='572a22000d408fb524258b379bf272a007c8da977c3e8d47c34f4e45dd7b1932'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-ppc64le'; 			sha256='4d1a3e89fdb7641422dc5cbcab48fd2da337b03265cb5ac2858c3425bacf952c'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-riscv64'; 			sha256='c45193b98c54e5a898e6b9095f70b0487599f19ce25b579ed2fcc3f868415aff'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.22.0/docker-compose-linux-s390x'; 			sha256='716aded74df512728638f1fe53170c46d94c1a085bc5a24108ce7101bc37bd81'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD ["sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
ENV DIND_COMMIT=d58df1fc6c866447ce2cd129af10e5b507705624
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 05 Sep 2023 23:04:32 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Sep 2023 23:04:32 GMT
CMD []
# Tue, 05 Sep 2023 23:04:32 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.6.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 05 Sep 2023 23:04:32 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Sep 2023 23:04:32 GMT
USER rootless
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd494fa26a8aad94a0d22885340d6ee599258b2e67c6c22f91ed6221294435`  
		Last Modified: Fri, 29 Sep 2023 02:55:37 GMT  
		Size: 2.0 MB (2024548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152366591504a2012a175b6773ee6dd24c70908a8974de4f78b436134dbcd209`  
		Last Modified: Fri, 29 Sep 2023 02:55:39 GMT  
		Size: 15.4 MB (15438727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e729a1bea6f35c00510ee459c2c20ac218b3f9ddf24db1722f8ba114316a2`  
		Last Modified: Fri, 29 Sep 2023 02:55:39 GMT  
		Size: 15.8 MB (15768048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4475640d4b9700b7c0796e86dd2a4f56d238090f5c88fefa616bc2c1996f6cad`  
		Last Modified: Fri, 29 Sep 2023 02:55:40 GMT  
		Size: 16.3 MB (16284423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479bb069c95302029a8fd7f34e2f92c9f722466cb004ec9a7de4f28b7b46b84b`  
		Last Modified: Fri, 29 Sep 2023 02:55:39 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66610116e5414dd019279d78145cb14c323f0cbe81df8f7b5d64e397d9500453`  
		Last Modified: Fri, 29 Sep 2023 02:55:40 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c755325432ecc6f0291cdf9d6ed427a37394f0d038e681043f311699948f8efd`  
		Last Modified: Fri, 29 Sep 2023 02:55:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0c0e07713e2f3cee5a3329a21eb1a5981b56e182e2e0022b94117f61c62236`  
		Last Modified: Fri, 29 Sep 2023 05:32:41 GMT  
		Size: 7.3 MB (7291301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca35f54c3fdfe6f07e99114da7da6eaf73108f3645d57177c0c013e45bec3b`  
		Last Modified: Fri, 29 Sep 2023 05:32:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c9535dbe0a254c9f3be0a12df7698fd3a9f7c70fbba77ec73e7ee051b71114`  
		Last Modified: Fri, 29 Sep 2023 05:32:43 GMT  
		Size: 49.7 MB (49688272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4327d02e6b198ebb1e88d40b4c8c8908467ec2c03e11154853f5874549659a6d`  
		Last Modified: Fri, 29 Sep 2023 05:32:40 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838c0131b9530932ecf043530a808d2924cf1c0e56ef8edbe347a428513affb5`  
		Last Modified: Fri, 29 Sep 2023 05:32:41 GMT  
		Size: 2.8 KB (2796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45653d9a845a8f7fbdb10e2e669b5c4a37113473ad363c476d55f16a8af74d1`  
		Last Modified: Fri, 29 Sep 2023 06:44:37 GMT  
		Size: 1.4 MB (1413159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75976bf1dfca70832d6f4f13a73c92cbcccf1c326c2f2c4949aa6b2d4aafdb`  
		Last Modified: Fri, 29 Sep 2023 06:44:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e4460c642e843a6154369dbb5b1d7a635a8cc20317ab771bc50f895f36e296`  
		Last Modified: Fri, 29 Sep 2023 06:44:37 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c93e6a480b01dff81a359398a0204948420a72542dd3f2a4c64f40b7164726`  
		Last Modified: Fri, 29 Sep 2023 06:44:39 GMT  
		Size: 22.4 MB (22448800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905be7660723d0048ae9e835597a258f170253deb37f7ed3721d852b77f87ef2`  
		Last Modified: Fri, 29 Sep 2023 06:44:38 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:015924c83c9267b66636694bb67b29aca4b5d42485ed434c6937489af6f6c16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.2 KB (776160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ba806232f743a71fd3238f0e6947f5cda9ae071b37303d68e6160bb3967927`

```dockerfile
```

-	Layers:
	-	`sha256:9416bf3579c038352e12099c8a1e979f495d40cfb2c02d12c50281caa87a79f6`  
		Last Modified: Fri, 29 Sep 2023 06:44:36 GMT  
		Size: 745.0 KB (745018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89219e5c8370e62850d62ab323ae051abf653a56b681609bfd2a42d12156c8bd`  
		Last Modified: Fri, 29 Sep 2023 06:44:36 GMT  
		Size: 31.1 KB (31142 bytes)  
		MIME: application/vnd.in-toto+json
