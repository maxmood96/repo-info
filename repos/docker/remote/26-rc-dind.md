## `docker:26-rc-dind`

```console
$ docker pull docker@sha256:6073529d51b127dd1a9c61f77a6e3cc382c94278ebfa3cd5b6fd5d723986d72b
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

### `docker:26-rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:09ff3918d869617cc41dee458141c859beac73ebefd879a2ab048e11321418ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127130295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebc48794e3eb4bc88bb06948224a90b745c3a6a49f819cff49e0c2dc3dc972d`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD []
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c70fa28bd47b8c239eb5ca27d77af0f3e6b5b4bf650a64371e0419ded7924d`  
		Last Modified: Thu, 07 Mar 2024 18:49:35 GMT  
		Size: 2.0 MB (2018462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0502d51f75eb2ea66cc609be7349e3e740ec4cd3faceca46eaa5634b6162a`  
		Last Modified: Thu, 07 Mar 2024 18:49:34 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baef5582a6338b59d71881630bcce8ce3f907d34e5810ec2441880406205f63`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 16.9 MB (16906057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233461d18016a0a6c93ffb091d10e1ef06111c13d77500f950b1da0fe9bba40`  
		Last Modified: Thu, 07 Mar 2024 18:49:35 GMT  
		Size: 18.0 MB (17982453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf1dc48541576a54aa37f8529d97a88d860686469b49ed8ffac5e613e7f7df0`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 18.2 MB (18214532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f65f978ebaf1d5fa25da63b46951536b129465205fccedc3fa453caf9d55a1`  
		Last Modified: Thu, 07 Mar 2024 18:49:36 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ad4da4b67d48d01078cba113e6b2b406a28647c77fc7cd1c04996b9f7638e3`  
		Last Modified: Thu, 07 Mar 2024 18:49:37 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0afa7b9f090e70420aa605519bd43bb03b6418ba4c400081cdb8228221bbd7`  
		Last Modified: Thu, 07 Mar 2024 18:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9f439c3eea295b7d5af8eb76e3dbffc1d73e3fa5b9cee3ff734c24c9b8e3d5`  
		Last Modified: Thu, 07 Mar 2024 19:50:37 GMT  
		Size: 12.2 MB (12156277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793e21a60173df2bf691ddce71f4fd989d764c59245795e17f5be6e3a1b45434`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 88.9 KB (88864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de50c4d8546dd08c5a062e15919f38f9eb3ee5b0ff00877aa160861b1444ff4d`  
		Last Modified: Thu, 07 Mar 2024 19:50:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5af86cb28f7c8ef72654ca668091ec196a405a1dcb92d09b1fde85618651f`  
		Last Modified: Thu, 07 Mar 2024 19:50:38 GMT  
		Size: 56.3 MB (56346596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c0811a2f803e3e506caf00dce1c75320912abf62355ed2a430448ee0404529`  
		Last Modified: Thu, 07 Mar 2024 19:50:37 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552d68de7cb813adcf455eea87227a8b3949979a84301d69b5649c428b485c0`  
		Last Modified: Thu, 07 Mar 2024 19:50:37 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:d8b3df9c2309cd7edd2750cb1dbae2e49f5cc1237ce5a1c76d4d384cd7996c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.9 KB (874907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3425b28fbe2db56159f05507b1beceeb657bff5e3e1dde0a811af4456bd2996`

```dockerfile
```

-	Layers:
	-	`sha256:7dcc185d91a735bb048f6de0edde753a1c501f4e847049d4f712effeea7a0b4e`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 839.2 KB (839155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028a8a90ae0b94190e1d22be16f81de8cfcdbc550c8175a775fb6acd30009587`  
		Last Modified: Thu, 07 Mar 2024 19:50:36 GMT  
		Size: 35.8 KB (35752 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:3ed76e12255c3650d7f08db9bd0376af424702b722b5e5da62b0161ada6d832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119057197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17994aa400c259ffcacd69bb93494508270b030826de2435a0fa993a44b2bbb`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD []
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b644515427b339d759c0893c759cef3712594a3f94e1032049e20c70b4e2b4`  
		Last Modified: Thu, 29 Feb 2024 23:26:53 GMT  
		Size: 2.1 MB (2108659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648ef94eae9908d98c672a4dd6dc6035976f446aca14300d96f2b66f828e7f52`  
		Last Modified: Thu, 29 Feb 2024 23:26:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ca0d5ec978deb82d5072316cbb86c5ef37b6f8f8202705b9e3592cde624ae`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 15.3 MB (15287824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2c3c919ec8fb7a0eab05feb72c9635b13c2dff0050a408cf45f68f484ee901`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 16.1 MB (16099978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10380a0d25fd7d80ad44fad3f5b6945dc100b907573c8921c1034a4e28f50f81`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 17.2 MB (17207701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e8d4125ef8699e0f466f81b139004e283429668e66ae320d1da174eaf2f66d`  
		Last Modified: Thu, 29 Feb 2024 23:26:54 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06babee6ea372f1296ff27e8348e0cd91583308cb4c6f799f5a5e915d362c089`  
		Last Modified: Thu, 29 Feb 2024 23:26:55 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0de69755a40dbf13c341a4d448b9b7ae721073e0f4f4aef9ba2c4cd0e475c6`  
		Last Modified: Thu, 29 Feb 2024 23:26:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebd108f9e15a37d2ceaec4d1c2fb0bd119d8e783d355b299a9492efd52d93af`  
		Last Modified: Fri, 01 Mar 2024 01:01:56 GMT  
		Size: 12.4 MB (12434121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c6df2d48f5d1a0ee61efe2bd37e2691b388d0569757db967bba3bafda0d0e`  
		Last Modified: Fri, 01 Mar 2024 01:01:55 GMT  
		Size: 88.1 KB (88095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb46db9148a4fd6120cc302894ed343abfc5a811ecd29371184393bd2e5497b`  
		Last Modified: Fri, 01 Mar 2024 01:01:55 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dabf27b16b266d1648b929493652a6227181b37671a845abf4397d3ae3d15e`  
		Last Modified: Fri, 01 Mar 2024 01:01:57 GMT  
		Size: 52.7 MB (52657101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89c58ddf191ad5de474b63fd1a329a03cdca71b663d17df9ba0250b3aeabb0`  
		Last Modified: Fri, 01 Mar 2024 01:01:56 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a882ad98cd5eb62e32790f1a880a59b8a0cf2c890750c0923522db06af0c9`  
		Last Modified: Fri, 01 Mar 2024 01:01:56 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:8598e356eae1ede142f3f53e04d05053fc8b9e8d411f87701b2dea281b025b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 KB (35746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8346e690f426b6115259e94aff8c988ad80cc4311feda35517718d79e140d16b`

```dockerfile
```

-	Layers:
	-	`sha256:ca349b7399d9c11c23ecc042d0b5b21f71e7ca3f5118ccf849a2a53db4016b74`  
		Last Modified: Fri, 01 Mar 2024 01:01:54 GMT  
		Size: 35.7 KB (35746 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:d481292f8564472ad8f45b8f94081584af720941f1123f833d423cb8ba4359af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.1 MB (118124047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1abbfcdc7d3ad65f01718829044ac5d0822619d561109de66275c28f0d06f6f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-amd64'; 			sha256='ddd69ee2ca3dd61760e771dcd2f3453dc677dfeb42c9484cc2321b96bc1b7c57'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v6'; 			sha256='6aea498b2a168bcd13f919e85e0670c2e5a71abab8ecd6bfe52874d14680f617'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm-v7'; 			sha256='1566b6f3cf69d06ade467d9928e19f6a6682182fe3008bc9a0c83385d5637fa9'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-arm64'; 			sha256='fa36eb4deab2fac6ddf5fdeddcf16999bc9d5fb1d632e0ba7e572b519df8a656'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-ppc64le'; 			sha256='aced23b7832c690703d0cb6339d4ccdbac9b45f0392b865b131aba9b572ae3c1'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-riscv64'; 			sha256='c15e51986d59398552b3ecd50b4ca75779e42c878e34761df54616ac02165207'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.linux-s390x'; 			sha256='c3578ab9814e4c2d0f917721b1dfd140b85e40602f6128745178a051cf4d0196'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-x86_64'; 			sha256='19c9deb6f4d3915f5c93441b8d2da751a09af82df62d55eab097c2cbfebd519f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv6'; 			sha256='c9fb575152f757a5edcce8ca0a399de6ba8dfacd80a8c730f56f0957cadb5858'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-armv7'; 			sha256='72ec3b7726b5784cf4ac14e2c32781f5090cb57a2951cfc59b24a74a88e9ce79'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-aarch64'; 			sha256='86fa6982c55e1bb741ac71ebbbb78c715224eeb46a820364ec6075cf87047d53'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-ppc64le'; 			sha256='236176989b202caebce42629d57f6faad310159c1c1b826feb63a097910bd0a5'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-riscv64'; 			sha256='eacbc70fd96c4c9a20bd58fc91a756372ece659211b9f566da33e15112c0b2af'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-linux-s390x'; 			sha256='23a643f8994c945683f62669cd0f44bc106d3312ea04c3dda39d7514f0b1035e'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
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
	-	`sha256:7aae121f4c6e463c253ea668f964dd5d7d26343756d552167d75ce8a755788e6`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 15.3 MB (15276517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538317b0a451c98b29c279b1a9dd9bfa7159c3f358c7f9ae0c7d50fdf815fa7`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 16.8 MB (16804267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c800e1fddcc64412702ff8067e7f649317cd262cb90e289e6e3c06c964f2d17`  
		Last Modified: Thu, 07 Mar 2024 18:50:37 GMT  
		Size: 17.2 MB (17204117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f339ab4d0aede8ce7731d0f324723b5ba0268ab2c3c598bd7a88a9dee4bfd5`  
		Last Modified: Thu, 07 Mar 2024 18:50:36 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fdf6a4e48f6f4f82e74aa36048a51f78a1d53681d16789d00483fc7f40125b`  
		Last Modified: Thu, 07 Mar 2024 18:50:37 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebaa99ef89d54676785aa2263f4fc4b7bb3486655eac4ba196e8273c83786c8`  
		Last Modified: Thu, 07 Mar 2024 18:50:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1bfbebba5787f8b66b4f55917d2fb74ee350b9844dac8a34d128f77dcaf8a`  
		Last Modified: Thu, 07 Mar 2024 19:51:17 GMT  
		Size: 11.3 MB (11274442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8928de332069c473825bb5c9f64bdcae589b372bd1a853321a7e5919257f6298`  
		Last Modified: Thu, 07 Mar 2024 19:51:16 GMT  
		Size: 84.3 KB (84265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344a21ab52a05362be5476bac2f9daaddaa98313f094cee9bb97bea3d30feac`  
		Last Modified: Thu, 07 Mar 2024 19:51:16 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82172e6b2b64865aecdc18c18fedf54c9d4ed0d366fc7da34b1eb3ad646aa5a8`  
		Last Modified: Thu, 07 Mar 2024 19:51:18 GMT  
		Size: 52.7 MB (52657081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0952cc6071521c4351374cb9f8820cfcb19140f008775df798361fae2ec59914`  
		Last Modified: Thu, 07 Mar 2024 19:51:17 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2395a045dbc1e34a4b013b2813580be7283cf5fd18f6d8804e0a6b772d8ac65b`  
		Last Modified: Thu, 07 Mar 2024 19:51:17 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:6e27b23f556f5634ec4055d1a49b89609e27e5019004bad5269490d3ff0d78d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.2 KB (877228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e620e32b9f01121aef4fea27eecb4aabf7051a1e8b032d326a16c14f60d354`

```dockerfile
```

-	Layers:
	-	`sha256:74a1c1e257681b9c5a1fd60f456b98bb5d4633a9e48a4fa50c93bdcb28960e8c`  
		Last Modified: Thu, 07 Mar 2024 19:51:16 GMT  
		Size: 841.3 KB (841267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:249fb892659dd35dc741cfe79a0d20a4fb2c89fa4fee15109756c7e061b694b6`  
		Last Modified: Thu, 07 Mar 2024 19:51:15 GMT  
		Size: 36.0 KB (35961 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:31b5005688785193bff94baa158820c2e09410f6239870dc66d1df8dce0978b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118290306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309b65a2921ecc7bfb8a209d2036a17582661298cd5231a5f1af588ea2f53e33`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_VERSION=26.0.0-rc1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.6
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-x86_64'; 			sha256='eca30ae32dc451f9e6d6c8ddce078a76f23b355c3ca0ab391d58f59e87c0d310'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv6'; 			sha256='9cf3bd154108919fe93e3b06045a88da83b06f2d7799f300d2101e836a593436'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-armv7'; 			sha256='14e1cae9322dee586dec2cf0026a2c039fd834fd6d27a14ef875e51f0aafe1a6'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-aarch64'; 			sha256='05b91fcc38d80378508dc42e027fa71f13431bdd3247139e51fa084e95c3de9c'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-ppc64le'; 			sha256='beb103c13748f381a6aee542ae15ca626a2d60867ddc20afa2409128affe83c9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-riscv64'; 			sha256='92a33146cbec3f4c02c5d967d21d28516b0273e34c183fe9133eaa82a9606677'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.6/docker-compose-linux-s390x'; 			sha256='1b4932489acfe35044eb924a1d6b4ed9047cd909b90b19008fb321998d9c178d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
CMD ["sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-26.0.0-rc1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-26.0.0-rc1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/var/lib/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 29 Feb 2024 11:10:50 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 29 Feb 2024 11:10:50 GMT
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
	-	`sha256:d5e373947c633ebf3fa9986ae70a2fd71f8df3215c7243e45124c067fd4548fc`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.9 MB (15917020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175757f58356331e958899b4d5e45a3f2b639ddec46c4cae57a44741ac538201`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657ac24788fe05605b760abd9d5b9b1fc663c92de3870c60805b00c0e29709e8`  
		Last Modified: Thu, 29 Feb 2024 20:00:13 GMT  
		Size: 16.6 MB (16640489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68660a4b8ae70fc6a495d7eeb9dfa4fe01328afae2cd6d9fc914c73c48ecb5da`  
		Last Modified: Thu, 29 Feb 2024 20:00:12 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838e1329e0d77349ff18111bf4a7f447953856f6fa0417674c5ff064a513d830`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3860585275b2dc666f25566e11b743ea4e441382777b0b808df04ffb5599111`  
		Last Modified: Thu, 29 Feb 2024 20:00:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1bfcd5098982cbf462e44f5c8e0c4352c15ef8c6bf730fde90c8ce7cb67d70`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 12.6 MB (12626950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846b2cd1cbd504fa292b54bd3e71a12de4de612779273a7c00a40f5442f1d805`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 98.4 KB (98380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38228a0e69eeaae700099f9d0baf37de2d6d74af7a0af4695c5786bf405d3422`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9aa3532f63c4d2696e64022bbb719f51bc72600935ef12dc5b4831fe970e92`  
		Last Modified: Thu, 29 Feb 2024 20:51:53 GMT  
		Size: 52.0 MB (51991143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79491999133f06d5a6f297ae143f1f04bb8fa4a172fcc315e382762916f138cc`  
		Last Modified: Thu, 29 Feb 2024 20:51:52 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e9e04ede7ff56ddc7a1ef7ea99408a6990935fb92c45e630518fafd09817b3`  
		Last Modified: Thu, 29 Feb 2024 20:51:52 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:3af26522f46f0c316eacfcec0399bb8951a470a2999c6e716195234064d4566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **879.6 KB (879622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256406c6a54e242dced9221cbb21180ddc2555309e7f2f1638cefad93a9d1bf7`

```dockerfile
```

-	Layers:
	-	`sha256:f74cb28ab3186d304a88fe3c82ae37b5e89580579b663f51551595f42a887348`  
		Last Modified: Thu, 29 Feb 2024 20:51:50 GMT  
		Size: 843.8 KB (843798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed7da8419f470fbc0f8ce91bb8c0b70e290a730408c13ec37f679783e416280`  
		Last Modified: Thu, 29 Feb 2024 20:51:51 GMT  
		Size: 35.8 KB (35824 bytes)  
		MIME: application/vnd.in-toto+json
