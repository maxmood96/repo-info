## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:392421f389a772848445647cec145ee10e0dfd06bc456ee34944c17c33160770
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
$ docker pull docker@sha256:fef294f654d446b28bb96a067c5552cd95434f737be1bd8f7a27f6fc42219172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146128956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5818569099d87cbe0f828c2031b538388d1d7177292e5b03ecbf8fa8cfb82e2c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Mon, 17 Jun 2024 22:51:04 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe01b594f40bdec3ca33c28b35f6c07fdcab95fbd6b3dde4e5a726487139f99`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c80050ca831a092bdc48b735d815a7ea2c5282900d0ae45b061524c464cf1d9`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6858cc868e201cf93e949fc5920c6c6e04704cd92e089f9b77eeaa95ccac15`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 17.0 MB (17029158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27568734f42c2ac0ea4f13c611238c102360c443c8c4c221bcbd1f7a861350`  
		Last Modified: Fri, 21 Jun 2024 07:16:22 GMT  
		Size: 16.5 MB (16538007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3b88164869014d66e282b9a285ab9ca07bec8fc74d1c808ce646cf82b5ab0a`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 17.1 MB (17137910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bbd3e2c7fbf8ea030a24c1975cef088975c5de7b2cc5b219047d0b7ef764d`  
		Last Modified: Fri, 21 Jun 2024 07:16:22 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b725b8573291a96ac8c860a0dfd3b5175eebe9ebd3973b248441b5eac3e5f64`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e886fccfd74bfd1df911faf3d086eef2e84e764538f90cb38525417383808a46`  
		Last Modified: Fri, 21 Jun 2024 07:16:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380d3325a0e22e9f15418709efcb6072fa2aa16abc4157f191b4aa2a0527a5e4`  
		Last Modified: Fri, 21 Jun 2024 15:52:22 GMT  
		Size: 13.0 MB (12991299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1d4bcc489a6335fc8447982a84fc6f7e590b73f3905fcbe1e8e986387e620`  
		Last Modified: Fri, 21 Jun 2024 15:52:22 GMT  
		Size: 98.6 KB (98626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88c1c9ee544b6331a09c45985509f0a695f7d7cc39ba0e1a3318e5069694c68`  
		Last Modified: Fri, 21 Jun 2024 15:52:21 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac35bf5bf925e8d6f405bab86ccc3f2b776e844c8cd150c2786504407f44f0`  
		Last Modified: Fri, 21 Jun 2024 15:52:23 GMT  
		Size: 52.4 MB (52369211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf55aaf1545a0e99aa93f6cd66fccbff172d5bc4908e23f369f152817611c0c6`  
		Last Modified: Fri, 21 Jun 2024 15:52:22 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd85af79c32b40301abc86000f49500db1d91ceb8377285b33d88763038a875`  
		Last Modified: Fri, 21 Jun 2024 15:52:23 GMT  
		Size: 3.3 KB (3255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b084e9bf3acd9ab2d90d97bb2526385ea7ca547f21eb5092a3b912e4bfadd1a`  
		Last Modified: Fri, 21 Jun 2024 18:51:23 GMT  
		Size: 1.0 MB (1023084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea03c8207571846487629e6ce783e9db20a26739ec45170a9e6a934160a8d6`  
		Last Modified: Fri, 21 Jun 2024 18:51:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb4314b75b8831cc29efdeee0a5234215b684a8c59e971c7fb95bf35ade8c44`  
		Last Modified: Fri, 21 Jun 2024 18:51:23 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672511cf7fac9e221797cc148bcf43f9397fbcfc74ce2b6038cfcd0b214b59b5`  
		Last Modified: Fri, 21 Jun 2024 18:51:24 GMT  
		Size: 22.8 MB (22836950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7eb6f84bd11e5cebc45fe625d81349aebc0ab50986fdc7ba2f12d60d34a016`  
		Last Modified: Fri, 21 Jun 2024 18:51:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a37236b078b9c95029eebaf9b364d574df1792840159d4a2476514f2e341a0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24fdf06817648ed95a1ab896a0d5478f2fc0eed2a82d34df8654cb69894cec0`

```dockerfile
```

-	Layers:
	-	`sha256:48e452311ca7a81230c7970903ea42f288e5f66a9744da77f096f65455acd49a`  
		Last Modified: Fri, 21 Jun 2024 18:51:23 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json
