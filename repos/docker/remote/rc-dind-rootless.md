## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:9c6bf2d2b224f3410a5c7eac981d7297aaf9744b5d85b0ce4be8148701491a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:6a797c4d02123f76ec77de91b872ca04555a87f137b185dfc8811fa0a8896513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141942357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb05c26d6f5b74224caa75c403437782bbfaff7087040e26a3fcf407c260535b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 23:39:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
CMD []
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jan 2024 23:39:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba5000a1254dde420992b6af6db58fdcd4862b79adf1d88b81f132f62c7d167`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 2.0 MB (2018464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f156c17dfe5733ec773b0a8cfd1dc6d7f6096db92373c153b0885fb9f6fa63cf`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8945a0bd73b35a234725490a60072a84c657d98a6faa0549ae178d7ac665cc`  
		Last Modified: Fri, 05 Jan 2024 01:53:50 GMT  
		Size: 16.9 MB (16891688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24fb2d4fdcd30abeef62a854a41648a9740e61edba2418218c9097844711484`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 17.2 MB (17195294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264e7eee16a1639ef22c918c9270fdbfc623240bdad2e3db56a7bc845b413be`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 17.9 MB (17852072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b887d8e287a3955a7a4f8e63c7c77f668e51ea73929ff8a4954f866cc83c051`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62527c10bf6536c092afc9edbec3656e62baf32146c682d0cc99b07e8df4b69e`  
		Last Modified: Fri, 05 Jan 2024 01:53:51 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74711a39693f3d9ea89259cabf9ad7a1db2fccd2498531e93c516ad01a59a4dd`  
		Last Modified: Fri, 05 Jan 2024 01:53:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6619ea13ee9b85bb69295b2f00abc9c3041744d84fb1a975ba529e265c77b71a`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 7.1 MB (7068082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03711b79e228ab0a994b821ff683ecba6d08ac4f416bc8bbdbd8d53c45015cc9`  
		Last Modified: Fri, 05 Jan 2024 05:47:54 GMT  
		Size: 83.6 KB (83644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a0fb7c5c631ce11c1f8ac122bf6c21988b2b8fa51b2725aad5dc83522a6f33c`  
		Last Modified: Fri, 05 Jan 2024 05:47:54 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b4eaf8a6b23aa41d376d870478ed953e416fecbcd6ed8c4d78f5ab25d6f1df`  
		Last Modified: Fri, 05 Jan 2024 05:47:57 GMT  
		Size: 55.6 MB (55578203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85da9a7f6d63f87b67f9f8d26709db974d91b0159aa247cc1e024cebc4fb47b7`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658182b0eab05036df69c43db069c862a87b7cbf39b5735812b163c13b396c29`  
		Last Modified: Fri, 05 Jan 2024 05:47:55 GMT  
		Size: 2.9 KB (2874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956cbaa3c64ad6cd2292862b5681e5719f2d86b417b677679eb936cdf151f1ed`  
		Last Modified: Fri, 05 Jan 2024 07:47:35 GMT  
		Size: 974.0 KB (974043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb78f5b9388698031e7d4b99f8828adb90978c5a95139a402688f3164f29fe52`  
		Last Modified: Fri, 05 Jan 2024 07:47:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee8ae1ad4f7ad9aea13714bb67854622d462c23e7570ff061214862f25b1897`  
		Last Modified: Fri, 05 Jan 2024 07:47:35 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cbdb683de3e150c6cc3051c6149ce360789efad5d7c248ee213c29788bab5e`  
		Last Modified: Fri, 05 Jan 2024 07:47:36 GMT  
		Size: 20.9 MB (20862810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cb4a101ac8cd8f65f0cca4a63686323af57a763b62c3b1f2403d9d8a342593`  
		Last Modified: Fri, 05 Jan 2024 07:47:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:a3c44226ae20c868a5cedde0fe77f1929c85463ae9d166ca1acc707a67e5e790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab1ee27a3f30011def0a519ad33fe637166309246cca96c4f52c4faaaa5d8ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b6275ee32b9e3f54bb849b8cb8aac593474b5fe337a9e999647c820ddf05b10`  
		Last Modified: Fri, 05 Jan 2024 07:47:35 GMT  
		Size: 727.5 KB (727468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7439d27c910e97e4ff02404120201e87303dd4ba38647f1b7cc4f3231ffdab2f`  
		Last Modified: Fri, 05 Jan 2024 07:47:35 GMT  
		Size: 33.0 KB (33001 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:be5a9004e930c719cabd1c8d347a036ff88e53800a10e6fefe6cdaf45461926b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135758555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e0e3c008967c9a33fbd272c9e4e7e0c0029600d40179c90bad99fde27c832c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_VERSION=25.0.0-rc.1
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
CMD ["sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-25.0.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-25.0.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
VOLUME [/var/lib/docker]
# Thu, 04 Jan 2024 23:39:43 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 04 Jan 2024 23:39:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 04 Jan 2024 23:39:43 GMT
CMD []
# Thu, 04 Jan 2024 23:39:43 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-25.0.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-25.0.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 04 Jan 2024 23:39:43 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 04 Jan 2024 23:39:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f7f5dfc78da18304eb4182d0d9812b54f9f67b404f702bb30a18a258d2e828`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 15.9 MB (15898968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2016098b7e4307df37c03cade0cbf5bb28dd430b00a643063b47d3b6db5ad797`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 15.6 MB (15640602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cecda7589ff1bc7873d2dc1c56d43b445f770594fc4ea3b7b9d1685214a58a`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 16.3 MB (16302321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c192c6cc697f33fbeecd318661d3eee7e68f97c3388f0f3600938a68e79dcffe`  
		Last Modified: Fri, 05 Jan 2024 02:15:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86ce5d0c34db276c50e408daefacb3a1ac83e1c6637f9700733ecccd5991a73`  
		Last Modified: Fri, 05 Jan 2024 02:15:02 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2e953f6ebfa7fa9a3670bada3a313c7bf0c980bfda49ec6833a8ce5ed04b8`  
		Last Modified: Fri, 05 Jan 2024 02:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6f7f4786f805712775b6aa1f98a3bac4626b6e244e917b290a1d6c6ab11ab0`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 7.4 MB (7428476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d3c9af1066d789d7a2e05047e1361c902e3e775ffd2032b9773ff3002d3331`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 93.1 KB (93065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f70fc3677175d4db06176178ac5e404fa737e2e8069c46652d0086981d226c`  
		Last Modified: Fri, 05 Jan 2024 06:14:38 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacddf5261725ffbb32419f35641934b5cb58554d1d00654bb6bc32fd3516512`  
		Last Modified: Fri, 05 Jan 2024 06:14:40 GMT  
		Size: 51.3 MB (51277484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d33235a00378c1b792a81b837dc1987ebe3fff28b20071a71d9e814634a399`  
		Last Modified: Fri, 05 Jan 2024 06:14:39 GMT  
		Size: 1.5 KB (1508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164512e13b197a35025576209798d17725fa0e2083ab5cc334daf6da37fc998a`  
		Last Modified: Fri, 05 Jan 2024 06:14:39 GMT  
		Size: 2.9 KB (2872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0411d8d0ad2447507fbec44421e135a4f3f512bff3f8d86314a3be05f0ede674`  
		Last Modified: Fri, 05 Jan 2024 08:13:42 GMT  
		Size: 1.0 MB (1016222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdee2e7f9d82a85d9d44d2e8344f5e3d885ff85f1d01a3a1753f194c02745b8`  
		Last Modified: Fri, 05 Jan 2024 08:13:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2155d3c0de4eddfc4f2e0d0fa16aaa65d50d54d3e21c6e0a8df65497a52856fb`  
		Last Modified: Fri, 05 Jan 2024 08:13:42 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51952509aff42639615e51c292c7439a7e049cd79cda84a2e3ccdd78f80c275e`  
		Last Modified: Fri, 05 Jan 2024 08:13:44 GMT  
		Size: 22.7 MB (22729152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e929d6c9a64f47f08b89b440485c8542a75435926e12a457da4d2973170ab7`  
		Last Modified: Fri, 05 Jan 2024 08:13:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3bd616f694e06ea740bfc6c0a6085199266727ab6cfd85cce5618360dd277ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **760.5 KB (760539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f99f7ba0486318718ecea3f7d4cbab557d921fef843fafcc112fa8dae157df`

```dockerfile
```

-	Layers:
	-	`sha256:3dd5f6a48fd80ce8233415f5bdac0448027986d06761603ab4b507d5a0b59db4`  
		Last Modified: Fri, 05 Jan 2024 08:13:41 GMT  
		Size: 727.5 KB (727477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d277e4af399ad373daace48dd5f10c8a5ceeede51912056a18543415ccafc96`  
		Last Modified: Fri, 05 Jan 2024 08:13:41 GMT  
		Size: 33.1 KB (33062 bytes)  
		MIME: application/vnd.in-toto+json
