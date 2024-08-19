## `docker:rc-dind`

```console
$ docker pull docker@sha256:2c54b91c59606a2fbd481962f208f302465103e4039ba52f58c13bba6f29da10
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

### `docker:rc-dind` - linux; amd64

```console
$ docker pull docker@sha256:fdebadc0625949042d4b10aade1989a6e3ee384053c79c078410d97f5b1e2ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130039210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264041620472c3c7ed72f5291cbb23fa3d3431099171d0c4c15300b266c81f7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_VERSION=27.0.1-rc.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD ["sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ee23ec764966a6692d523f5f07371e2a1d28fa06967581758be098733c881c`  
		Last Modified: Mon, 24 Jun 2024 22:56:12 GMT  
		Size: 2.0 MB (2010471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553c2850b516d5db6b6ece728e7022224c1118cb309684ac57d85e45ab679022`  
		Last Modified: Mon, 24 Jun 2024 22:56:12 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368e8fcc5c6e1783cbc032313b98559064cc5772c18312f27970a68d4fbcaba3`  
		Last Modified: Mon, 24 Jun 2024 22:56:12 GMT  
		Size: 18.1 MB (18074778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d802f3a2e7fa4065350ce2a197b80925564e3045353420ef82e0c010422ccd41`  
		Last Modified: Mon, 24 Jun 2024 22:56:12 GMT  
		Size: 18.2 MB (18178850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb872415551155d606e4dff156a9b0a19414199bad73a198ade5b295a34a46`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 18.8 MB (18792461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd6d5936dbd4c30355c792b9afff62d7d1b4ebf6e42d898703868b809adab08`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8168a5d58d73df6439f3f1f1426fb8457ef3bf0372523b53d94928bef0e385`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4f296566eed88298388da73f717578031de21f15fa0b309133a8240e95114b`  
		Last Modified: Mon, 24 Jun 2024 22:56:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4abe3c29f2b067a3f9368fb563f9fac69bf47027156522a4d784a6f4ea03524`  
		Last Modified: Mon, 24 Jun 2024 23:57:50 GMT  
		Size: 12.5 MB (12504368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130fdae106900b1929bae9899ea525b5e1a3b923cf788f87e252c54a3eb0ed99`  
		Last Modified: Mon, 24 Jun 2024 23:57:50 GMT  
		Size: 89.2 KB (89184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a199671fb3e9f7b4e9aa700ea0ad5ef5e231628fa1530456c7d40c34d3765e8`  
		Last Modified: Mon, 24 Jun 2024 23:57:48 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b724af85f7611db5e04ce4517e15bea8658a7addc0b0ff72af6a582550fa62f`  
		Last Modified: Mon, 24 Jun 2024 23:57:53 GMT  
		Size: 56.8 MB (56757293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71c0806e0b7bc2f55353d54bb683a4040c837bbea9fee776ec62b1c0b091d70`  
		Last Modified: Mon, 24 Jun 2024 23:57:50 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee8866df67c20b85ddd6ec12589dd76a71bd09695d5a3a568efa11eeffe5663`  
		Last Modified: Mon, 24 Jun 2024 23:57:51 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:087a6f60c9fbd968f933e7cd2bb214716b594582b0ed1a2fa4c37f8b45c87568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 KB (34047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1400d6bb63b110a419a4e851aa726acb175384c53ea27c3786f89bca81a43970`

```dockerfile
```

-	Layers:
	-	`sha256:cc28d0ac76592ea65012cf9939cdb452de84e5552c72551986b40d4993b8fbe5`  
		Last Modified: Mon, 24 Jun 2024 23:57:50 GMT  
		Size: 34.0 KB (34047 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:cf60663856efd1630d5907f63cf7bc61c6a679062b5136d6e617b50e85510bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122397265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb1d3290e265fe233fa237babb0ddd2a0119ab49222d8937fff45bba18a90d9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_VERSION=27.0.1-rc.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD ["sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d023b0d86d5f3c29ffac412805754ac7366e4ecc23c5177010d36847ad55a7`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 2.0 MB (1993299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d6b44884f2fa15c4e561076223287af9c44c7cc4621122e79f252f814684c3`  
		Last Modified: Mon, 24 Jun 2024 16:53:23 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a08ef681858d3f01be3f76f5eaa7c85fa1da5082dbc0cc319a79735ba587ad`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 16.3 MB (16344460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0090752c608d2b7c887fa8a44502c06cc5dafe74731c96b0fe2c3f9adc822d`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 17.0 MB (17010826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046941150108eca7f67b54ba19d21a4c8b1c34848e625412ee7205a28fd8af1a`  
		Last Modified: Mon, 24 Jun 2024 23:37:47 GMT  
		Size: 17.8 MB (17751794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec97fd238cfd05b0857e3957bcd33ff27f25ba27383028ea2a0fc99497f90ab2`  
		Last Modified: Mon, 24 Jun 2024 23:37:46 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e239da9532ecd0fcc7286370cf7cd2c0acc7a0e94657b9d8db3fa3726022fdce`  
		Last Modified: Mon, 24 Jun 2024 23:37:46 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0033631991719a0464f0ab0f5ce3fb536d4af02b40e9059d1990f62ec3a49392`  
		Last Modified: Mon, 24 Jun 2024 23:37:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc35547b02d62b952a3910c66116d662e963508d552c83db8c2ee6774ce6d0f`  
		Last Modified: Mon, 24 Jun 2024 23:57:59 GMT  
		Size: 12.8 MB (12779973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ebdd5d51b867987025870fb00139881d5fdfab75c82cc0b4bb7d778c1b70c0`  
		Last Modified: Mon, 24 Jun 2024 23:57:58 GMT  
		Size: 88.4 KB (88397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfe2b28c3d8a91e21e4070173a18d73860c0e2b082e920e524a0e3787fc4eeb`  
		Last Modified: Mon, 24 Jun 2024 23:57:58 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550a8cb51ca5d4eed09e153c9b8289c113c842533e49bea966a5c4c2b35cac42`  
		Last Modified: Mon, 24 Jun 2024 23:58:00 GMT  
		Size: 53.1 MB (53053391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64071fb51dc7e591b08c478c93473926f3b21515d308790584f669ee1fa5f28d`  
		Last Modified: Mon, 24 Jun 2024 23:57:59 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8342a7ba449ac97529fc28bc1bbb2efbb6d01e2b1875c9f43913aa5c676308f`  
		Last Modified: Mon, 24 Jun 2024 23:58:01 GMT  
		Size: 3.3 KB (3264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:7584072329e0086942d4ae9107ba8609a498acf285a4bbce47797b945bbffbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e5493edb2dc123f3ca159cd081244c69a5186c1627f9aa667ffc28443e68ca`

```dockerfile
```

-	Layers:
	-	`sha256:560e8d20b2c059826d4347a078663470ba8e94d361c4b7bf2dacb51724930be7`  
		Last Modified: Mon, 24 Jun 2024 23:57:58 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm variant v7

```console
$ docker pull docker@sha256:73f9788de949a919c3822a8665028b26b53dff2ec17dcae51b4c2ca9d10aa6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120748134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dac955fc18ea0a87fc31e8d262401492d49033123799e12e84c6131ec188199`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_VERSION=27.0.1-rc.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.0
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-x86_64'; 			sha256='359043c2336e243662d7038c3edfeadcd5b9fc28dabe6973dbaecf48c0c1f967'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv6'; 			sha256='398d717e6cc9515ca0325035cfe626cbaaa1023754cfd22c13eab6b29ecc2d54'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-armv7'; 			sha256='604c00f22176ca8291f43d22f066cfcc89f4c09de2113d287f72c0bdcf611e46'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-aarch64'; 			sha256='296076f4d14d2a816ad750f6890355fc118692814e4b4542942794817f869d37'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-ppc64le'; 			sha256='c88c097fa475f07140c01e3ca370a503b927f377f200114fa17e0bee6e0cbc4d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-riscv64'; 			sha256='b563b99c5a1c03a1a83cb56ea1f7a492ef74e137afd0cbea485b828b6c61dbe5'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.0/docker-compose-linux-s390x'; 			sha256='f701bd64dc5b204352c788931b43de9c778d47eed1be7caa81b57fc47a09164d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD ["sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3be0ff3f8430a7c5e4c0602a3a190116b4a4d4d1d16b89c627d5436d8d3318a`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 1.8 MB (1841225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e90c200cd38a52aed6f4457d4fb93031e32aab75a2c05019a3a2dda9db6b7f`  
		Last Modified: Mon, 24 Jun 2024 16:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb755fd46ba8be39c37074bdc8778c82778acdb1af8434d1404456166132219f`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 16.3 MB (16336726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24f5075d7a1c1c966789cfd6c0a00ec11d9ec063c0d23d09adcd6808b8b1a4`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 17.0 MB (16998029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9e479a6f88b8467dd8cfc0675ade5241e4cc443db9b52234334ac885ff280f`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 17.7 MB (17737536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eab426e7ce487450b94b7007d5078b2083e2d671d5d781b6ed55b8046538a9b`  
		Last Modified: Mon, 24 Jun 2024 16:53:25 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31dd28ce1af5a7c84e79f474ba29edaa351ab049bad9d407ff4b89f021d6dd37`  
		Last Modified: Mon, 24 Jun 2024 16:53:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73e169e1e66eb6716a44e3d4c680696f43c52dbfd6e656b9346f7ed9d4d51f`  
		Last Modified: Mon, 24 Jun 2024 16:53:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42bc33bc036e0e8f805234398b230ae8e1709b69a03904cc3b4f27240537af7`  
		Last Modified: Mon, 24 Jun 2024 17:55:52 GMT  
		Size: 11.6 MB (11593915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0c13e63e708b9f7b274bc88092c86de200cf8af508a9e6b66524338f266f67`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 84.5 KB (84467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a418be2a963a2b4cd006a1638e685dcd47208d0e05b1dd21f112f011bea54f`  
		Last Modified: Mon, 24 Jun 2024 17:55:51 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa06938a38f6c9818a92ef644dba20514935368a3745db376db5d1cc3478fc6`  
		Last Modified: Mon, 24 Jun 2024 17:55:53 GMT  
		Size: 53.1 MB (53053416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61ea3dbf75cfb1b7b2d43b48204088fb2f5841f133e19ad68e6c02b853755d8`  
		Last Modified: Mon, 24 Jun 2024 17:55:52 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1adb5da40bab52a4078e4ed15a7ec23d02d3fa0d54b9a1387cacf997134a835`  
		Last Modified: Mon, 24 Jun 2024 17:55:52 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:715577fef942d9122b74718caff521a5267307262ed296fa397b43c78d3d000b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 KB (34249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41b97331d8b34f6be580fa5489617f14e482d8a7b1d2e48f8e6eaf7ff69f358`

```dockerfile
```

-	Layers:
	-	`sha256:70f01d078110d421dc0737e091ad09fbb737146160f7838e881f3b380ac8b36c`  
		Last Modified: Mon, 24 Jun 2024 17:55:50 GMT  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:307b1cc0a603d0debdde7d20610a9c58028b94a91f16ab9fb63e6492677ea930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122290144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414414fc71cb2f6384d75e49ab1d566f893ee8d8ccf72a4563c3467430f7b338`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_VERSION=27.0.1-rc.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD ["sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.1-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.1-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/var/lib/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 20 Jun 2024 23:04:54 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 20 Jun 2024 23:04:54 GMT
CMD []
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1043de68f70a9f12e4034d7a432f4583cfdd32926d2c8e09174b96ff2edc4167`  
		Last Modified: Mon, 24 Jun 2024 22:57:40 GMT  
		Size: 2.0 MB (2006600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31bf6cf7392daeec79e28441f18b15d0c838659dda02b7a3afc0cb2dcaafb0`  
		Last Modified: Mon, 24 Jun 2024 22:57:39 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4278c5606c8e213ac01c173c5d6d8d2b9cb7e1332e03bce706198de826ee76`  
		Last Modified: Mon, 24 Jun 2024 22:57:40 GMT  
		Size: 17.0 MB (17031901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a487e61d22ccbd74318d7f30d0e063c1dec4858fafb1b0ecc62f405b578a6aef`  
		Last Modified: Mon, 24 Jun 2024 22:57:40 GMT  
		Size: 16.5 MB (16538008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae27915f1f64662eb5bb5de1727f1d2993dbc701747b8d12b89fe7137e348345`  
		Last Modified: Mon, 24 Jun 2024 22:57:41 GMT  
		Size: 17.2 MB (17151897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc32768e32539269d689695db638b4676a55ed54b2ec4a6df94027e6db071c`  
		Last Modified: Mon, 24 Jun 2024 22:57:41 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1408614e10170276d0894269fd482b9a55a717a5eea01a7e5c5a19e7f031f63`  
		Last Modified: Mon, 24 Jun 2024 22:57:41 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0596b04f488ca2d68fd73039428c590e164f85f027423ea9014473e942382e05`  
		Last Modified: Mon, 24 Jun 2024 22:57:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d8e8c20db843459401b9bbdeac7da067102d6aa756f56906b078eb790e9320`  
		Last Modified: Mon, 24 Jun 2024 23:57:39 GMT  
		Size: 13.0 MB (12991272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2ab55759f4222562d462660e6e13b11f89b854b1023737bdb92cb91624075b`  
		Last Modified: Mon, 24 Jun 2024 23:57:39 GMT  
		Size: 98.6 KB (98629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a4f93b14aa1359a422fc8fdfcd646f77b0ef456bfbaa7db0e4faf77b801696`  
		Last Modified: Mon, 24 Jun 2024 23:57:39 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7715fa6dd5978818c8155ff17ea73fe6dafc74173b525c35e24a60493fa1684d`  
		Last Modified: Mon, 24 Jun 2024 23:57:41 GMT  
		Size: 52.4 MB (52375078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db8c4145039418a669080d2624eb61d532323d6af54703851880832c73b4a1e`  
		Last Modified: Mon, 24 Jun 2024 23:57:40 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cffd41f2d31982e50e8cc2da7bb5c77e22dcd9b787017fb3c9bd3417eb1feb`  
		Last Modified: Mon, 24 Jun 2024 23:57:40 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind` - unknown; unknown

```console
$ docker pull docker@sha256:4e722b68a34661b4282a5e5661aee6ab7c3310e8efd91f1ab78a528153efbd7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5e6a3ee68ad183c4e444de447a4715c23c22276178c0f66ecb284492db7658`

```dockerfile
```

-	Layers:
	-	`sha256:fd10dee32f44e71c3fbe0fec7b3400e62ca0e21ba3f53995f798e72f4d54aef0`  
		Last Modified: Mon, 24 Jun 2024 23:57:39 GMT  
		Size: 34.5 KB (34522 bytes)  
		MIME: application/vnd.in-toto+json
