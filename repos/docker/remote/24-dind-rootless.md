## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:54bf8de13c3520ebf42f6c77fafcc95a2e7df0f701043bc16c04a63d0029ff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4b228cdf8a7b80d5353db892a1eeedafd9e9242ca8241313f0abbc6d72259f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efd9e029477a6ba7276963ce74381c3e91376e3232da15143165b5196323362`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4f76e3a90f62a8c5ca873581e3e8f28d444b96f943aa335f784361f3f5212b`  
		Last Modified: Thu, 20 Jun 2024 23:59:23 GMT  
		Size: 2.0 MB (2010462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f253291606f48f10a81cde2e83de164d3af65f91f7b280c51913ca9e345f84a4`  
		Last Modified: Thu, 20 Jun 2024 23:59:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6880d4eeef18bad680c7a1efac227acef1864d8cbbba937c25347a5aa8e40a89`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 16.4 MB (16410666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6777a79d00a7173d08c8dafe2a5d7c4faa732261db617eafd6e56a9bf46a1`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 18.2 MB (18178850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d13a55c91d119178eb5d2a5c4d37171ff667abac1e818b0c549f9eeceff187a`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 18.8 MB (18770948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28030efc338d61ba3068ff249376d2080e6df5338a0e189f76113bf1ea99d16`  
		Last Modified: Thu, 20 Jun 2024 23:59:24 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9ea6be471518295e9b902dc2fc342207911c8d12e8c9472e26c5f3918705cb`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3f49bf3cfee990cf139d87453b204bc3a65066023c40c77debbc0145206414`  
		Last Modified: Thu, 20 Jun 2024 23:59:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedf8c72dc7fe9a770d0dd8d0fb138f271f07c97b59a61b10648db1167a5c85d`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 12.5 MB (12504290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27450857966d0929370cf45369fb93234b3f3157a462fa7130bfc0ae4e4cafb`  
		Last Modified: Fri, 21 Jun 2024 01:02:46 GMT  
		Size: 89.2 KB (89184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbdf4109703eb8d3f5df95ae6399c3e1ecc6102496a3f1671dbc2797b9153af`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e28b440e907596487beb98b51c7d880b57d6d3719e9ec8d2170a6c9178e6d09`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 54.7 MB (54740517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb64cc101108ff22eb4871388e87d808859f30ea993b2ab0bfeb898e8d97937`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e1831d1c836eef0b9f69cebf436e241f02c003525d3a1752059742e4077ce7`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a839b617cadecd3a1a1d2ad96929b04c779c760b80717194d45f106d3a57a`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 981.0 KB (980954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8878dcdfb41923bbf4109efaa5d09dabb3544eb081b413d7d932dbbb6c2282`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e64b3f547173d4bd0a0214e9e6634d0dcd2b53cb8f912e46c372c15cbc7261`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76da315d499b98f3c83385d4cc9b7012cf6c88a2ca1e7ef7a5750fafdb3fa8b7`  
		Last Modified: Fri, 21 Jun 2024 01:59:32 GMT  
		Size: 20.7 MB (20676197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447ea9f3d77802c35e545c058172fead2b24bb1b022198996ee3cc34bce32fd1`  
		Last Modified: Fri, 21 Jun 2024 01:59:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:30610ef5d0efe3fa774608c4c7de3f73fbcd2faaccb8ea31f0f07cd84c9e1c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0db1ebd0b7231041692b9e2b76fcc27dabe843b91eee5b2df4d2555f7ff77cd`

```dockerfile
```

-	Layers:
	-	`sha256:cef46f4a985fe0cbb6275c18664640dd4c277bc08b1bc412441829dc8fbd436e`  
		Last Modified: Fri, 21 Jun 2024 01:59:30 GMT  
		Size: 30.3 KB (30274 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:29baa3e83bb82dacfb190ecbeba0f9271601c0149c6ce8962962dedd42a4b756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144731350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c57eb9d83a111371096535311a249738ed24dc1575b1c98dbfcfc856b12daf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 01 Feb 2024 16:06:26 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["/bin/sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD ["sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.9.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.9.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 01 Feb 2024 16:06:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Feb 2024 16:06:26 GMT
CMD []
# Thu, 01 Feb 2024 16:06:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.9.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.9.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 01 Feb 2024 16:06:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Feb 2024 16:06:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0782eb4e77d74d9b9a314d9b56833c86c46848b438a32b37ea5557573243ce67`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 2.0 MB (2006611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8746dd4cbb23fdb5e4bb3f089b9f4b73a6bd3204e0454cd67ed85adb2827ee50`  
		Last Modified: Wed, 12 Jun 2024 18:30:18 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d251f23dcd036bc3e6e8a42754613b59bd37eb5936c06882d857738b5370a210`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 15.5 MB (15459110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b347aa6775503e62c9f11acde6b8159ccda5c6324c2652b01c5fed538d98abd2`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 16.5 MB (16538684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f0d74103b8922b37a8b32ca7992eae11401ccbe6c3df4e7a33321c851c5ed`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 17.1 MB (17144869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48ae2d0907a46dfa08409c9101f0edb6103164f673961ede20b345da062739b`  
		Last Modified: Wed, 12 Jun 2024 18:30:46 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27298211e9a62e57bea436de1c78f6bf37f07d6b1bf6e34740a57ac3bab58f7`  
		Last Modified: Wed, 12 Jun 2024 18:30:47 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468e87477176c1ec0821b3350c6111affbeb5ef2c69ccd9456c218534d0d6009`  
		Last Modified: Wed, 12 Jun 2024 18:30:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2833bb8ce8f3cfcec0bb819590bacabc28d75d3e90249428059502445ecceabb`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 15.8 MB (15812001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374127e549047629fa05a1b3daf0fab4fbdfe3e330fba5c6b1baec6a5dd0de0a`  
		Last Modified: Wed, 12 Jun 2024 19:54:11 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fa3c2e278a048e4305947bc4a709f9a975c368db55397e90bedaeb295ffa85`  
		Last Modified: Wed, 12 Jun 2024 19:54:10 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ac91f01471a00f246e5611c261ccfc90178c1d13af15a99e6543cc16be053`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 50.1 MB (50076180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8016491d82678b83f352596f53af88ab39c7b746b79283de813b6b992505d3c`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103ca35ed5aef2cb3aeb089c775813fe30862320be8d34a4e572895a603703a9`  
		Last Modified: Wed, 12 Jun 2024 19:54:12 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e437b9085ed98cd25d07b8d44d0ccb4e3bf3f7f1b04453dedd5d43068a1eed64`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 1.0 MB (1023084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e085bd1343b5329aadeba463b1438ef0eb4426e18128e37664b38142e1e20bde`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba91246384a2f28b7fce8db10183b00a752e5ad7d2acbecd23de3c8c71ef8a0`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d406738ffb64ba495afd63ad263d4cd872f29086d2ec6245a8140149f806f27`  
		Last Modified: Wed, 12 Jun 2024 20:52:41 GMT  
		Size: 22.5 MB (22476094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7034c58e12ced50bdf2f0c40b4d9a1eef566d5df692b286f429d01522047af1c`  
		Last Modified: Wed, 12 Jun 2024 20:52:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:babe3c12bc10ec44c937ca38125e81d04654e74ea229ba773bf27e9bef131af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd36e7131bccad0726c4a58416aaea3a880c0c1322f06dc8ac5283e9cd99bff`

```dockerfile
```

-	Layers:
	-	`sha256:277fbb3b9248dce976f06d56c7bd5c7804877ead66ab0980cadf59f311e0d8e8`  
		Last Modified: Wed, 12 Jun 2024 20:52:40 GMT  
		Size: 30.7 KB (30687 bytes)  
		MIME: application/vnd.in-toto+json
