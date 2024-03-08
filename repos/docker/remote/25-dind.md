## `docker:25-dind`

```console
$ docker pull docker@sha256:305e9247aea279651f13ef0119510b74d75122a629206363e370749feae94e28
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

### `docker:25-dind` - linux; amd64

```console
$ docker pull docker@sha256:d2d238e914613ed9e3be4c4dd6bed7e8f0d67bbb2b48e215c13fefa4b8e65747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126439319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c60c33fd23fc289e3d696bae0394f2265b5c52d0dc0f63775e56afc48b1fe7b`
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

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:2103b9621855244f29bc9c49da9036dbc6e448ea7d1940fd37a47ac78b7901b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.4 KB (877401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e4740c25404b72f22f81a7fd8aacebe9be8ef1a71385a9a51ac63018bfc8cc`

```dockerfile
```

-	Layers:
	-	`sha256:d2a7d3639bd078715a47cf8e04e513965d6ca2967f24a3e0a911d3a38aac0239`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 840.0 KB (839950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae6adcdb545adc22256bff1f50a71e17496c9fde083083b2c626756c25abb5d`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 37.5 KB (37451 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:0d0baef7130f14745e4aa8579cdd0b87cdc7c41b9610d9f0c376eb40744e2b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.4 MB (118416239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8315918245b12a66ce969bf8b45fa292ccb277165414ab1f86351e1a008b2469`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_VERSION=25.0.3
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 15 Feb 2024 18:06:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:06:03 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9750b5baee21696c1d4bcf08650bbaeb2e50e98089f8b9ae4e45de64e7d6fb26`  
		Last Modified: Fri, 16 Feb 2024 21:33:59 GMT  
		Size: 2.1 MB (2108644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74beaaf291473ce2eee086edd302928529070c429d6a967ac64ca69097f6ee7`  
		Last Modified: Fri, 16 Feb 2024 21:33:58 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856bf45dbe72a3f7a3556390425b278db4d7f4322bdbeb3348a10498dc73c106`  
		Last Modified: Fri, 16 Feb 2024 21:34:00 GMT  
		Size: 15.3 MB (15273059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2de3a0ea565f5e239f212a23523a6e82c66c69bb659814a91f6ad820e43a01`  
		Last Modified: Fri, 16 Feb 2024 21:33:59 GMT  
		Size: 16.1 MB (16099983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45252f3e7d9c36391d18d77fe9cb9e0c042c4f04e04952aeb4603154fedd979d`  
		Last Modified: Fri, 16 Feb 2024 21:34:00 GMT  
		Size: 17.2 MB (17207702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73995007d8620b74629cd5e40cacb790f3e51d04d6a2cef3c79836d38f32b588`  
		Last Modified: Fri, 16 Feb 2024 21:34:00 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb4fc5aa9e0f71a2b9fc1ee0a2a324e5937034ff424bf6a13605e0483e821e5`  
		Last Modified: Fri, 16 Feb 2024 21:34:01 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff2966ed3e5c52a00d23357d6e9f37e2e32a23596db0895b2d415c796ad3e42`  
		Last Modified: Fri, 16 Feb 2024 21:34:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecc2dbd381031590016db611f140890b014b54e7e05ecd7d1fa81392a03fd33`  
		Last Modified: Tue, 27 Feb 2024 21:51:24 GMT  
		Size: 12.4 MB (12434126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec4d19b3d175ac125c7d7ddab6a6fc098fd75093a0f730f18a91abd99cbd0bb`  
		Last Modified: Tue, 27 Feb 2024 21:51:23 GMT  
		Size: 88.1 KB (88103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec6f1d8a1d0243bdaddcdf91f1746f22d7735f73e78289cf933165abf2f3a1`  
		Last Modified: Tue, 27 Feb 2024 21:51:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891dcb41402883ee3087f7c61007045ed86cc7104e4a876897fa18f946062804`  
		Last Modified: Tue, 27 Feb 2024 21:51:26 GMT  
		Size: 52.0 MB (52030901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de1f24c0df6be9006b3d9fa2f49de2b854c2e662d14c230424ee00c8cee8517`  
		Last Modified: Tue, 27 Feb 2024 21:51:24 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb480b136231222ab25e2e1c99347d89552bedce3ee2b6b40731d60eb1f70ba`  
		Last Modified: Tue, 27 Feb 2024 21:51:24 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:0a68925700f7aeaab88cc96ba028fb02258aec4c275d110f44243a4ffdde9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a7a0c625b04031f6ffc69a7854845ac73fb1ac222581935062b014008d64a2`

```dockerfile
```

-	Layers:
	-	`sha256:c01707c4fbf30335e69e63955e708b8256c6ce0a23c2a23618527be63ebff172`  
		Last Modified: Tue, 27 Feb 2024 21:51:23 GMT  
		Size: 37.5 KB (37492 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d9484f5fb8b07fb09a3c8e25dc3047fa84c23fcbbf8d85bf726ffc146aedb7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117495659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeb233554c4be8f4588facbbe8edcd4b32fc68e3cb8569fa22b22625747f00a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12baa34c4b3af0d924c08f5c0364298070ad555de60b11bb8b9d270e51fd6ad0`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 1.9 MB (1896140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce178a6d07ef665083e0bb7a5011401991ac2ce60e1dd3674325bffe854ab5b1`  
		Last Modified: Thu, 07 Mar 2024 18:50:35 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6232ec3733d1c618309d62b462edd0f1b4c32738e17955969422d9a9df3101`  
		Last Modified: Thu, 07 Mar 2024 18:51:19 GMT  
		Size: 15.3 MB (15273191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce7750f1f65a5234d750dc5acf6f0a6fd40fd566e73526b4ba8f8c2600dcad3`  
		Last Modified: Thu, 07 Mar 2024 18:51:19 GMT  
		Size: 16.8 MB (16804279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2718e21880331bbabf47f48dea6126ce043242e1bd32130465575a88520442`  
		Last Modified: Thu, 07 Mar 2024 18:51:20 GMT  
		Size: 17.2 MB (17204121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a2b803a1e186debd00e968960e0acacee7ecea3fe1c4901d00a0eb9f55b840`  
		Last Modified: Thu, 07 Mar 2024 18:51:19 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c15a53e9c96b0d236fa3359495dfe3c3525c2092a2e19c3e53e8f72881c892`  
		Last Modified: Thu, 07 Mar 2024 18:51:20 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf450a2233a07e21b4bac2254fa67fa495d1a386782cd14c60fce051549f1c`  
		Last Modified: Thu, 07 Mar 2024 18:51:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900bee0818419399f536f7eaea7e187a05eb773ba38e961fab87e4fcd8259394`  
		Last Modified: Thu, 07 Mar 2024 19:51:59 GMT  
		Size: 11.3 MB (11274368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190bc85a7f67df2912fb01d7c15d3170f29766613ae480048c7f5ff93cebc68b`  
		Last Modified: Thu, 07 Mar 2024 19:51:59 GMT  
		Size: 84.3 KB (84270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a8473f671ad866ee0975f34ac8f54de964c09ca8f5d5ce397e85ce09e37334`  
		Last Modified: Thu, 07 Mar 2024 19:51:59 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36e43c5900c9f159b2a24291721527143a56f0a5db3f51979e5d1d4455994cc`  
		Last Modified: Thu, 07 Mar 2024 19:52:02 GMT  
		Size: 52.0 MB (52032069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59e4f31dd8b6c7e6e4365a9dcb6729382abc1a48dc3f5de880cc3d02417a438`  
		Last Modified: Thu, 07 Mar 2024 19:52:00 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6eec3e2212be2c677b7ffbc29c2878811c769e9fd8577ed6424dde7937e13`  
		Last Modified: Thu, 07 Mar 2024 19:52:00 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:25ec6fab17272fdf0f99b9dc9ac99b10f2d52d7b701f585f1545772b151c9df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **879.8 KB (879817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034120051a34f714f7b3ccacaca2ee9ca804ff64b5c40f351309bd56a267ccd1`

```dockerfile
```

-	Layers:
	-	`sha256:2c9cff1f2812879f41dd263295d0550b135ed7ac8a707f46dc460b2722c97783`  
		Last Modified: Thu, 07 Mar 2024 19:51:58 GMT  
		Size: 842.1 KB (842110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:821887faf6321f7e9eabdb45e2778022b5f90da3236a6091f1501338a55b4baa`  
		Last Modified: Thu, 07 Mar 2024 19:51:58 GMT  
		Size: 37.7 KB (37707 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:25-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:331e10f05080546a4d9b02136a36750fe914fab82105ab61f326d68d040da59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117639188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ef4b20f79670e86bb888d755583347367b6c291fbc0a336f3c86d4bdff5885`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 15 Feb 2024 18:06:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_VERSION=25.0.3
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 15 Feb 2024 18:06:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 15 Feb 2024 18:06:03 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 15 Feb 2024 18:06:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2024 18:06:03 GMT
CMD ["sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 23 Feb 2024 19:50:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Feb 2024 19:50:50 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2024 19:50:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 23 Feb 2024 19:50:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2024 19:50:50 GMT
CMD []
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

### `docker:25-dind` - unknown; unknown

```console
$ docker pull docker@sha256:f6ef4fb74b61954267b762999b52c24efe12264382dc0779cb3563e8490e67f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **862.7 KB (862719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57531b9592fd27198904748536ce9a39d661ef728cb9b5547601fef623be29e`

```dockerfile
```

-	Layers:
	-	`sha256:3c757d4cf3b834370219ade70687b000a43a954123d0e538921c3c141a57a6ec`  
		Last Modified: Tue, 27 Feb 2024 22:17:10 GMT  
		Size: 826.8 KB (826755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76d18e35f1208fc0a8787f04c22ef6f0332abf57a1e3dc9a84528ffd8297cc4c`  
		Last Modified: Tue, 27 Feb 2024 22:17:09 GMT  
		Size: 36.0 KB (35964 bytes)  
		MIME: application/vnd.in-toto+json
