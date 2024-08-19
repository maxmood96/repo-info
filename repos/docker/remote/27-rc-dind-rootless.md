## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:240a1bd0e3535dc06df456c9e1b1422a1fc032cb7a4f918c445fd57550b18465
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:ced5e8de5f18ae5d97c50da037e2d90b54f41b3db909d308414d346a1ff224b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152003895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade792bcc354d89fdbecdd7dde8688dae0c02f96ff5f143ed37f9ea6804741a6`
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
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
USER rootless
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
	-	`sha256:3cd67fdc638f6e2cdcd00e3edd9d8e5e002ef69bc3709850f9867171aeab7587`  
		Last Modified: Tue, 25 Jun 2024 00:50:21 GMT  
		Size: 981.0 KB (980955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0d6a4de2acfb969b8cd79fbfa197237bf0352a01c1029539c4a7c4ebcf4ed3`  
		Last Modified: Tue, 25 Jun 2024 00:50:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5d639e02ea497af8c35e8da3f173e6fe88701237bdb195f03528ec458768c5`  
		Last Modified: Tue, 25 Jun 2024 00:50:21 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d5e7759abccb36ccfb45c36c557d55ef8fe5d4962b54d46da05f051a01c5ca`  
		Last Modified: Tue, 25 Jun 2024 00:50:22 GMT  
		Size: 21.0 MB (20982374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0594305f600e622c206eb75d1dc0e30e41af8112cc6c5801d2d42babe8d903`  
		Last Modified: Tue, 25 Jun 2024 00:50:22 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:658feb490c2e544f3ed8ee58544f223d67596c8224fe4f20d13a9e5d80135995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5271c5990f113cc2a4d7c60face97e7856dd9b4dcaeb4576354670bb22d391b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa0bfabb97026bb065c44b9dca34943aee7c3bf735f0be06f5e7a6d74e48f67e`  
		Last Modified: Tue, 25 Jun 2024 00:50:20 GMT  
		Size: 30.3 KB (30338 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8a327b98b430687c995d8a8aab43995d229be30e0b65fea515c7fc06784120de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146151527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8679840334c1e32b10237f3b26139fd6665efbc30bb0265857dd6fa79b7582d`
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
# Thu, 20 Jun 2024 23:04:54 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.1-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.1-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 20 Jun 2024 23:04:54 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 20 Jun 2024 23:04:54 GMT
USER rootless
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
	-	`sha256:ca168c7f3647f12ac2932b137d394d79995b164d9a808a329399c8f363e6eb9f`  
		Last Modified: Tue, 25 Jun 2024 00:50:16 GMT  
		Size: 1.0 MB (1023082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3b6c00780d53d75735ac635fc58347e9e49b7d685d633ee9ff2f7b0dd35691`  
		Last Modified: Tue, 25 Jun 2024 00:50:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853015520b78bbd5cb4ba75fc93dc9e845eaa8f3c9a43e728516b518bd40658`  
		Last Modified: Tue, 25 Jun 2024 00:50:16 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b497fa5549063292d6b3f947338381b3f2be9572a051aad1229cb69e8408b8`  
		Last Modified: Tue, 25 Jun 2024 00:50:17 GMT  
		Size: 22.8 MB (22836945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef16114cd1aaacebaf1d16e65830e42697d2db9c9f0dbf8cd503c0c503b7b3f2`  
		Last Modified: Tue, 25 Jun 2024 00:50:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:7e086ffb719955c741c8d9dec612d396cb23c76e79065616a5dd3fb28bd991c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d00391f94f0022a894984b034cf96417a25c0764c3cfeb3033be6588976274b`

```dockerfile
```

-	Layers:
	-	`sha256:576d05c949a195eda8842ce331fb52c26cd301f8ac7d5d0257f623082e102389`  
		Last Modified: Tue, 25 Jun 2024 00:50:16 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json
