## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:75933ec8bf6413c88d9c63d49f259f47340a75432cc12f48c135e6caa5bd061c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3b40e9f0cb38514c1d80c3c300e7a0c132aa3a099056627a2dc2add11f7735ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151973125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46a0703af1fa962a4333fe0dab325ceac83b942697b0a76d9758c1ad16844ac`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 17 Jun 2024 22:51:04 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8b33ee29814bcd7e403ef1b8929a89b75decadf5c00c697f4b40e26a34bd18`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 2.0 MB (2010479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69091f1b731d79c0c3ffa23a3ea2185244670eb2c361167c5b930b69086f65cd`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec03a51f222338ae6fb4931b24b2b34f2c0a66421bba6ae7cdef246d1475e9e`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 18.1 MB (18069006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724707ec6497f2c777ca139e84343c4d624c0a10aa956d6074ef24c25fb00b82`  
		Last Modified: Thu, 20 Jun 2024 23:59:10 GMT  
		Size: 18.2 MB (18178854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d96ba145e08bd218ab4539e6ada14c7b315d4d7a009f845853e56c91370a989`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 18.8 MB (18770936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a0379d05541021105172cf5be25aa00d4871aa675a01bdc597a28392bf522f`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c8ed5df351b89acedf744ba4efdd19ea5bce58e281b153beb28b2485c35226`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df29db38b76fd8f3e9f3239568a5b8a9e5e38d1853a8c3f092095004489189`  
		Last Modified: Thu, 20 Jun 2024 23:59:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af55b80715b291f86bc6c23927f61f706d337b4dcce9d9ca659eda435198e5`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 12.5 MB (12504294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c0926b2e029563a3c12b852954bb43c72ef5b34ea7279574f25158b3385b7`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 89.2 KB (89186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12304a5053a0ea1d98a7ad4f951b851cf117271b144f40ab7e41ba16e4dae0c2`  
		Last Modified: Fri, 21 Jun 2024 01:02:47 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800438bd8f0d81d0d91b1d4ae026888dbd5ae22dfa83295e1995088792e3e6f4`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 56.8 MB (56753891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252775dfd0c3735ce76115db7bc5e9d7c94ec979496cc6b669985b806cae6b46`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c4d37555e57cebec72a9bedb66c67083077f39da906dd7388f1171eb27e46`  
		Last Modified: Fri, 21 Jun 2024 01:02:48 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c69637253a89655393c6c85d3e929a8bce78e38723b6ade00fc46c1097f3a88`  
		Last Modified: Fri, 21 Jun 2024 01:59:29 GMT  
		Size: 981.0 KB (980961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f7fd70412bbb87fba4639e40cd6ba2e7f63b607265368e3f7445948b8e905b`  
		Last Modified: Fri, 21 Jun 2024 01:59:28 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b8d32a2f23a05697b8f39977d4e349074fd7ba4fbece009ba08e424ff2214`  
		Last Modified: Fri, 21 Jun 2024 01:59:28 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3943e9cf89684e3480fe79d835ce57081ab37b8d871e774154330f5f6f93ae`  
		Last Modified: Fri, 21 Jun 2024 01:59:31 GMT  
		Size: 21.0 MB (20982373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3365bbe14f4f0e2499b02dc41ebc963035946fd7ad4967321a08012feee387d5`  
		Last Modified: Fri, 21 Jun 2024 01:59:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:cb944c9efb5b62d5af0511de3d726f0970bdea11dda564ee15dbd9c4490ca99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a64db597331c9efc88f2177032308eb5d04aefab8c28ef79698ac54c26f17ce`

```dockerfile
```

-	Layers:
	-	`sha256:e06895c73b32e4a190374f8b689910193d05df810252d2b3b3445aa4f0a5d7ed`  
		Last Modified: Fri, 21 Jun 2024 01:59:28 GMT  
		Size: 30.3 KB (30338 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:59b8e6ff4ed0ab48e89dbd12c690d8c124176a1311615b6e26441852c68759f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148955369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec959cbec510abfd8da0f39ac98429ae64adf221f3836be9975d299e8bdc372`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_VERSION=27.0.0-rc.2
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-amd64'; 			sha256='6569bb8b026b56d49a31aca80b61b4d0da1dbbf23ad6c925752790a9a350c9c5'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v6'; 			sha256='78627fe5baeef2ea6eb50a2a1206c5c479f8984f6637c75825c79f6a4b93fea7'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm-v7'; 			sha256='e48879480cf6dcfb76a743577b94a548d15e152b0d4fad82e12bb27f11ba0b26'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-arm64'; 			sha256='ad23578106a3a4f0a7bc9d8bdc9ba9155fa7b19889fba46f8f2c59fb10ab73fb'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-ppc64le'; 			sha256='3ec0f7f76a7abd93b2dfaa5ff314357113a66bce9eea205e206545de34a97471'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-riscv64'; 			sha256='6afcab070d6f939c13d9c1f3aeb9083fef58cb91c22d0b174f9dba7a6549a219'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.linux-s390x'; 			sha256='3fbd476b321d8b844358f796f3158a2f6df78d4d16acc2fc8a82265a2642c39d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-x86_64'; 			sha256='ddc876fe2a89d5b7ea455146b0975bfe52904eecba9b192193377d6f99d69ad9'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv6'; 			sha256='5f244291153cdd7facfe5007aa37f393d139c245b870025b8e86ef88a8de2705'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-armv7'; 			sha256='9dcfa9523dc912370417b7ccc3d81900bbb98dd9addbff0d218398bbe9078bbd'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-aarch64'; 			sha256='16e93b9c2fc147d29ca1acbb8ceab6a50a0e26af777f43dc7a753cb883142617'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-ppc64le'; 			sha256='f351bfdbb6bb9d18b33672ccba6dd31c53a3bd1b81f9e9052fc6d9125e7d5719'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-riscv64'; 			sha256='9940bd7533bcbd087d5301b8348136bc8922aa75739e3e359d8367e2f6dd7005'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-linux-s390x'; 			sha256='6f4b6bb51987b2f61b91cfe4017a8d162e86b82ba3ae074b99b06a1ebe4387ed'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD ["sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.0.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.0.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/var/lib/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 17 Jun 2024 22:51:04 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 17 Jun 2024 22:51:04 GMT
CMD []
# Mon, 17 Jun 2024 22:51:04 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.0.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.0.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 17 Jun 2024 22:51:04 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 17 Jun 2024 22:51:04 GMT
USER rootless
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a37c6920cf419f019cc2ece413c620d2c2c0c024b4f0c6e947adf6f650c0d32`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 2.0 MB (2006612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cbf91e38cd25c76a4cf8d25355d629193815e2234ac234d08474c3f47d241`  
		Last Modified: Tue, 18 Jun 2024 00:10:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebe42042517502c0a4214ec067e5e805812571248eb59007767634d4626c284`  
		Last Modified: Tue, 18 Jun 2024 00:10:11 GMT  
		Size: 17.0 MB (17029163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb7eeeea5f866d8f13beb04dcd0031ccd9fd374689779d555f0746a8fd0a7fe`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 16.5 MB (16538686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9f866f2e1c6ed3778e7a5e207db02ba4ef4dfe8a6482d489f68539d0418a0`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 17.1 MB (17144849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ee42643cc834ef80264a74abff8cb77379bede35cda028db368b8ce5558b2`  
		Last Modified: Tue, 18 Jun 2024 00:10:12 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0628e85c34c1cbad0cd6daef18eee405426305a16569c2fad2eee104c3432`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa64d3a7abb094e57b17ffec25482c5d47d599a88fb847a1b788e9afda51bd`  
		Last Modified: Tue, 18 Jun 2024 00:10:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d087116c8c715dcc196689ef1890a21a4cb6ed678f02ce5a5cf7c3d27d453f0`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 15.8 MB (15812082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0077b1d5de1ba5bb5fdb530b4cf8ab206d445ae5ac92d400c6b9d4aac257eeb3`  
		Last Modified: Tue, 18 Jun 2024 00:53:07 GMT  
		Size: 98.6 KB (98628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d4c824cc7d38d27b3cb58f35826c784abff2b247be745a903af8b6a3b0f98`  
		Last Modified: Tue, 18 Jun 2024 00:53:07 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2f7edae1a6c565c3a42fd9673c9f6c998e3730c179e7f77f3a492fc3a86d36`  
		Last Modified: Tue, 18 Jun 2024 00:53:09 GMT  
		Size: 52.4 MB (52369220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c93abac44889ca87b8ff30c14bddfa261b3e273b12a2f6c4adb7a9d31f6b8db`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192493a6cad163c9396addcfe00b3e7460a5838b9eb86967c2dbfc291c9dd238`  
		Last Modified: Tue, 18 Jun 2024 00:53:08 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eda00693e5a4c4869a7c39018b4edbf85d15bac9e5c8533b68b10ac5ee20415`  
		Last Modified: Tue, 18 Jun 2024 01:51:23 GMT  
		Size: 1.0 MB (1023088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d597b6cf8e5ac1eefc59d354de420e670dc2e409c4db3ec09f52a782b0ff657`  
		Last Modified: Tue, 18 Jun 2024 01:51:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00f1590922c08fa2e2e637c84cf8fbe705f293a6fb918c1c2d20423ead63383`  
		Last Modified: Tue, 18 Jun 2024 01:51:22 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc89e50921b9fb77631aaecf111779267844afcbc4ccd4b85de5ab72577f4cfc`  
		Last Modified: Tue, 18 Jun 2024 01:51:24 GMT  
		Size: 22.8 MB (22836951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e5a3fb91191215dae1809a9a166e6276211ad369045852d4f0f2825bb5311f`  
		Last Modified: Tue, 18 Jun 2024 01:51:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:149bfb15f3f73ce4002ccb2419c5d2eac71bc049e36f413bbc4a4433c8ef4b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbaccd2b6e45a2234316a828f1dd7e54f0f4698a75300e78d64c435833d68c3`

```dockerfile
```

-	Layers:
	-	`sha256:0ee6481e27d328c6c8ed0dcc68d37d4a953543691778b901b09bbcd3db84e379`  
		Last Modified: Tue, 18 Jun 2024 01:51:22 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json
