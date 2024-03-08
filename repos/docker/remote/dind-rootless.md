## `docker:dind-rootless`

```console
$ docker pull docker@sha256:05e000cdea864c647d79aba3f1e69d8226a3efef28337284e92a3ecf5040e3f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:4258d660fd34b2ac2e8931f6b2ac7475d27963a66f1152f714e0c18b4dbdd8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148408199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7935b259c4a715e7205bb405acdf238ea25e4a4ff8f546d789b7c75ff04cc6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.4
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD ["sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 07 Mar 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 07 Mar 2024 12:04:26 GMT
CMD []
# Thu, 07 Mar 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 07 Mar 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 07 Mar 2024 12:04:26 GMT
USER rootless
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482602742300e82b9bb1adcf771658989e9c20f5947a8c01e60f516d81dcf4a5`  
		Last Modified: Thu, 07 Mar 2024 18:49:31 GMT  
		Size: 2.0 MB (2018467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74b0467a17bef483ae8600c26a79f38a29db01662eec2328013f71baef173d7`  
		Last Modified: Thu, 07 Mar 2024 18:49:30 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c282e3f92e63898a22b0d2e85680452cd4b168963c4caf10c0ac2fd711573db`  
		Last Modified: Thu, 07 Mar 2024 18:49:31 GMT  
		Size: 16.9 MB (16902843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e849924e7d905c2116355ab721e67f83d3bf280ea5e519831cfc012d4564b36`  
		Last Modified: Thu, 07 Mar 2024 18:49:31 GMT  
		Size: 18.0 MB (17982453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cad5e1cb56eda4a9011b21529676035a585bf438b960be68feab0ff0620912`  
		Last Modified: Thu, 07 Mar 2024 18:49:32 GMT  
		Size: 18.2 MB (18214532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540ba4b4f1561fa401a73c64654f82b4e4eeea396539012a2358cb1577420de`  
		Last Modified: Thu, 07 Mar 2024 18:49:32 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f561a4b2d32a11276a3eb02f471e46247671f3e21e18753f3a641234d5ee3e`  
		Last Modified: Thu, 07 Mar 2024 18:49:32 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd7db794e11154a4a80337d6736753ccdb75fdc99a96633f25773af900a18c7`  
		Last Modified: Thu, 07 Mar 2024 18:49:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eb1e49e9d2d504423bd0f5b69aec5371a2445bf2d8c70d612c98f72c99f936`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 12.2 MB (12155997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f266a135960f3076ae407d3262a4984f22595a9a80cf14c4b91ee00a8d7555`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 88.9 KB (88863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de50c4d8546dd08c5a062e15919f38f9eb3ee5b0ff00877aa160861b1444ff4d`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1dfb59bff5f76d0001e52f7b5e775ef3986dda2f28e73fb792e2d94b02f4e0`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 55.7 MB (55659118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833108d18ae9dea51869a77f4d57a5d2f92d792f9e027010c3924c79bc79424d`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae8fdc5ff9de9e2fc92e0375798dc3b83cee90e757192de7cdcb852f4b23c5e`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1d45c83aa582b54c349acf51ead2ff2bcd1e73a1d4d28fe89a0527c0aa3773`  
		Last Modified: Thu, 07 Mar 2024 20:48:16 GMT  
		Size: 981.3 KB (981314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c656fb2569433f34cbb2b98333b005a045d17292dfac1a9116974d93627a3e7e`  
		Last Modified: Thu, 07 Mar 2024 20:48:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7639c863fae54ad1d16c806d594c89f42969e301a5b851b7c80300cc2579da`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa7260d50bb62de522747bb683a25ab7857cdb6f92ca22b1a24c8cde9f55323`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 21.0 MB (20985933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd482cee4163307b3f51da17b1c9fc74d64b6319ddac5b048129dbb5e77bf01`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:78d42d4ca0601662ac1b430477c653c22995e0d061e7ad7684bfdd73fea8b329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **919.0 KB (918960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4554465baee923431895ec85b1e5487e00244e142f5990a8e85e3a9251c4f194`

```dockerfile
```

-	Layers:
	-	`sha256:b01b48121b2349d487c89e115ffe71f9076f9b111ddbbf7b4bcf91069a10de53`  
		Last Modified: Thu, 07 Mar 2024 20:48:16 GMT  
		Size: 885.7 KB (885704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1ae098d3030513a17e1db11efd1626a8e12a9ae19fb3d6e213672d516f02e01`  
		Last Modified: Thu, 07 Mar 2024 20:48:16 GMT  
		Size: 33.3 KB (33256 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4992211b7f56b44a9ec73764e675e7c58fe2aebfb95917e04f2e5511319d460e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141498290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16d26be8d0919df83b92454f5cd6a275e424cafd5943468b0a404215a949349`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_VERSION=25.0.3
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 07 Feb 2024 00:56:51 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
CMD ["sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
VOLUME [/var/lib/docker]
# Wed, 07 Feb 2024 00:56:51 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 07 Feb 2024 00:56:51 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 07 Feb 2024 00:56:51 GMT
CMD []
# Wed, 07 Feb 2024 00:56:51 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 07 Feb 2024 00:56:51 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 07 Feb 2024 00:56:51 GMT
USER rootless
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd627277f8af1d68caa52e5725c89976aa4c6aca5c14958e83eb2143390ab6f`  
		Last Modified: Sat, 27 Jan 2024 17:51:38 GMT  
		Size: 2.0 MB (2019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb61f641eda83263d0ea571074960545636883de036a62c02d9b400bf583b3`  
		Last Modified: Sat, 27 Jan 2024 17:51:37 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733caa8798619f3c785aab636db1c660bf8ceee8e77ed49cf3970f3f30c48be2`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 15.9 MB (15902172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b482f87146141bc3e2bedcc4a540b3bbb60ce0e2066e192b06baa1aaa64e28`  
		Last Modified: Wed, 07 Feb 2024 02:22:59 GMT  
		Size: 15.6 MB (15640606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffd3afa1d3effdddb0b7e31a7cd39e3e94cd96bdc4a5ed48e796be9f66324f6`  
		Last Modified: Fri, 16 Feb 2024 20:28:15 GMT  
		Size: 16.6 MB (16640439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d13b96e2ce43240c9c9186b956f883e140b17694a75dc291ed5d6564282441`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872b0ec9e92a0ff66e85293db6870897cccf3d0277ac9bfe3d3af60841cd7f3a`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a41040cfda23c170d5a25b35ca4f9ccdab85d729c61312cc7e1be223b27bb32`  
		Last Modified: Fri, 16 Feb 2024 20:28:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12b5842cd88fe780f03562a537937f35d2e947c097335c95930973e40d09b63`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 12.6 MB (12626808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09fed680ddf104d1ef2eadf0004d63deb0a457f0ed8576f5e85a8ea4eed41ac7`  
		Last Modified: Tue, 27 Feb 2024 22:17:10 GMT  
		Size: 98.4 KB (98376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f799a7b288ef62f942732f0105e9ffaecb4f8237e75f6a9b37677ea506ba88`  
		Last Modified: Tue, 27 Feb 2024 22:17:10 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b711c26ad6148d3481de6d5410dc876f1323572fa12cf726c78694c1e2dec4a8`  
		Last Modified: Tue, 27 Feb 2024 22:17:12 GMT  
		Size: 51.4 MB (51355055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce59fe0e7942c27952508f6c230946c013a4fbd9fc38cd49f80db7ee631dcae`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 1.5 KB (1507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c26fbe85d26b0157fd68ad78ac224e507b8d6bfbd9211312f287ebaefc86971`  
		Last Modified: Tue, 27 Feb 2024 22:17:11 GMT  
		Size: 3.2 KB (3248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b793455d1d20bf712b0fa28f6fbb855c717d341be45ef57a0a483b6161705f`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 1.0 MB (1022480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5925033c44f541841f34349a1de8c4bb3dc0b255c80b705e8948354d71e7cf`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a0b37bc01627352479dba0c47b3df6cbc2e8f7d4b1bc769cfd2fa6989175eb`  
		Last Modified: Tue, 27 Feb 2024 22:58:24 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89caefe18b443d99e3ffc1227439a2e23679c66f7dc35533a449e1e6953ff42d`  
		Last Modified: Tue, 27 Feb 2024 22:58:25 GMT  
		Size: 22.8 MB (22834981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeecc04f1ac663e613349967ff5b14b96b11dcbe2f4e7720c222d235b0a3777`  
		Last Modified: Tue, 27 Feb 2024 22:58:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:1798540903c74fc565e808024eb6a0e602acdd0a25f030e009a3df7e8ca3f8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.8 KB (905818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9f9257f5047652ba45a9c70b555b55b23b3e2a5e6e0f8cf46ef3164a43f0b2`

```dockerfile
```

-	Layers:
	-	`sha256:cc4a4abf673d51c91458909ae23b992d7fed26ae8889bd9c0c791e9caa897c27`  
		Last Modified: Tue, 27 Feb 2024 22:58:23 GMT  
		Size: 872.5 KB (872499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30b308a9b94354b551622418d35d6cb7505f82e86ec7894179db99ec451cc69`  
		Last Modified: Tue, 27 Feb 2024 22:58:23 GMT  
		Size: 33.3 KB (33319 bytes)  
		MIME: application/vnd.in-toto+json
