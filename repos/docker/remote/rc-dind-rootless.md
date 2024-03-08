## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:85406141170c598058dc6e16c5a8265119beaf8ba89922ddc647d7b04f47cdf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:df07ba21fe3544bab203331eaa6c6fb31563739f6decbd1942d3e3b14d9ee959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149088276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f5ea563798ebf85d9b1348697b9467a3abe69309989a4f3325caf0a74290a5`
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
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
USER rootless
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
	-	`sha256:55dc454b7facb4fb8933ca8851aa8886d8ddbc7981f8d73912003aab8644ff71`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 981.3 KB (981313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b4288ef9255ad238146305b4a94c022ccb9aa7b0eaceadc85adfd40dd93485`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4fe2dba95e1cbaa365c8fb68ac3ed26f78128e27fed1bf2b02b10a9953d2a`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69227d9cfaac26566f5797c595561d691147d313458468a57b8ce07f20864b2`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 21.0 MB (20975032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc76fd55376f36fbb2d3cabb6462730d02c15821f825c04e977316d7eba5d7`  
		Last Modified: Thu, 07 Mar 2024 20:48:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:218035b87952ef58ac26785ffce435a499afef0a90d543ccc7ad3290fbdcb76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **918.9 KB (918938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f492f61c6b73481d9953bdf79159d5d388f02a8446ed24019e1b9bd33ca27d`

```dockerfile
```

-	Layers:
	-	`sha256:4d8f7e8d31a30588ddf12419325e877988c7989784b1a17c647f390f8f70cead`  
		Last Modified: Thu, 07 Mar 2024 20:48:16 GMT  
		Size: 885.9 KB (885943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c16c4302d670efc4e41c2952e39ba10374646e3f794d32e5aa376b032ca0a1f`  
		Last Modified: Thu, 07 Mar 2024 20:48:17 GMT  
		Size: 33.0 KB (32995 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:ed70ddc53127ef7d74478750a4adba5a8b9b6da263f2ee3006c63dc60d0ae393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142150352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36d32e2c362d5a54ce841d8b7a606c579e69aeeb97baf48943f8316fcf05784`
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
# Thu, 29 Feb 2024 11:10:50 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-26.0.0-rc1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 29 Feb 2024 11:10:50 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 29 Feb 2024 11:10:50 GMT
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
	-	`sha256:a214e8201d891d391bbcb27271023a864c6b9e19509104c2eb23421fc0b908e9`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 1.0 MB (1022484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527bdad640253616209795b96bc5107284daf67bc60649f4de1602611ed23e4c`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664cbc703840d12f569a67e25e3ef07c71cee5f7ec8a81193bc5f32e009a4dd`  
		Last Modified: Thu, 29 Feb 2024 21:51:25 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11020a95d9e85b79e9cd9da860775a58809718fa697ed7c3fc88c9bc2e146b0a`  
		Last Modified: Thu, 29 Feb 2024 21:51:26 GMT  
		Size: 22.8 MB (22835927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d423be4e0add4d69a6b38a77ae1fd57bab68141acb68ff6191297ee910098f6`  
		Last Modified: Thu, 29 Feb 2024 21:51:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d2e66acddeba45495e892f462527316e32d5500deafb14808a1c86313ccecaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.3 KB (923255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490a15fe5af617574411c2d773c08d748349604dfe35a6c15ff0411ac1a3249b`

```dockerfile
```

-	Layers:
	-	`sha256:fcf03dc2f7f5e25971465e75c93dc62ce3a14adb865f95e5df31a49b25052ec2`  
		Last Modified: Thu, 29 Feb 2024 21:51:24 GMT  
		Size: 890.2 KB (890200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec6fc8529b3d23294f708e4a525ae280463e09693ca9e1a47e35bc6d44835fe`  
		Last Modified: Thu, 29 Feb 2024 21:51:24 GMT  
		Size: 33.1 KB (33055 bytes)  
		MIME: application/vnd.in-toto+json
