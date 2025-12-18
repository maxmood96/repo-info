## `docker:29-rc-dind-rootless`

```console
$ docker pull docker@sha256:76cdaf83954352476728126813a5d862853de172fce9285469acaa6ac3ff156f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:29-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:f50c8782242b42ec0212e1241fcd64e31d67ce52a8853a0b8f6ea3c862394e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158298943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a7e97269e130e33ffe26c5565445b8d6a5faeb4d7618079347e31a5ea8730c`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:58:08 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Dec 2025 21:58:08 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Dec 2025 21:58:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Dec 2025 21:58:11 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Wed, 17 Dec 2025 21:58:11 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Dec 2025 21:58:11 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 17 Dec 2025 21:58:12 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Dec 2025 21:58:12 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 17 Dec 2025 21:58:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Dec 2025 21:58:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Dec 2025 21:58:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:58:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Dec 2025 21:58:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Dec 2025 21:58:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:58:13 GMT
CMD ["sh"]
# Wed, 17 Dec 2025 22:09:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 17 Dec 2025 22:09:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Dec 2025 22:09:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Dec 2025 22:10:01 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Dec 2025 22:10:01 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 17 Dec 2025 22:10:01 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Dec 2025 22:10:01 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 22:10:01 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Dec 2025 22:10:01 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Dec 2025 22:10:01 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Dec 2025 22:10:01 GMT
CMD []
# Wed, 17 Dec 2025 23:10:14 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 17 Dec 2025 23:10:14 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 17 Dec 2025 23:10:14 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 17 Dec 2025 23:10:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 17 Dec 2025 23:10:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 17 Dec 2025 23:10:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 17 Dec 2025 23:10:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a394fb7c8c203f2cf0d7f53e6bdf09a8424e5548cb8f826caa26a3190450e31`  
		Last Modified: Wed, 17 Dec 2025 21:58:34 GMT  
		Size: 8.4 MB (8399651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6436fc25dbb417c0ceca8afc15b6e786a22d10018c9b48fcd0381ffff7d79e29`  
		Last Modified: Wed, 17 Dec 2025 21:58:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d844074b2c85bb285438621003cec861e4e0c04db4ae8e5ff9d1f2568ce3c3`  
		Last Modified: Wed, 17 Dec 2025 21:58:36 GMT  
		Size: 18.8 MB (18766155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60003300dd4aba54a0c5bf821da67b895f1ad242a8e0952ce2da88efb8ab933`  
		Last Modified: Wed, 17 Dec 2025 21:58:35 GMT  
		Size: 22.9 MB (22905481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe73af2b914b60c02c48a3fcc747a62f550dcf1c94b982051f3cbd5aeee1539`  
		Last Modified: Wed, 17 Dec 2025 21:58:37 GMT  
		Size: 10.8 MB (10784464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0df4eee8063924e4d69a45ff49a7814efdb9a5b496771c22fb717805e5155`  
		Last Modified: Wed, 17 Dec 2025 21:58:33 GMT  
		Size: 537.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7437356ac0e6a024f88dda5ca6ff9642526dd223d2898b942b4250068af3a`  
		Last Modified: Wed, 17 Dec 2025 21:58:33 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ffa9b35bb275fb70beb6bba014bc495865accde38b14e22ac4d10469db48d6`  
		Last Modified: Wed, 17 Dec 2025 21:58:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c736d05342005ac63aad467e559092efdf84a39c3486e185e2cb9dc9f5c832ca`  
		Last Modified: Wed, 17 Dec 2025 22:10:28 GMT  
		Size: 6.9 MB (6933798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0daf8901f68c9953af66d76b4a6b61ccad88cfaf2648c0e357ccd994dbed56`  
		Last Modified: Wed, 17 Dec 2025 22:10:27 GMT  
		Size: 92.4 KB (92449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb342ea333d6880574469adcac48c4d3808a1a1c3dd187ac9804c060b3e9a4`  
		Last Modified: Wed, 17 Dec 2025 22:10:27 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b019fafa565c08f4e6219678fbd0821db8146cde5e9380b5f6052709b55f02`  
		Last Modified: Wed, 17 Dec 2025 22:10:37 GMT  
		Size: 65.8 MB (65757216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeddb11df2c42defd70c679ee739a6505da3cde2f66e3094e574deda26bbe65`  
		Last Modified: Wed, 17 Dec 2025 22:10:27 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716f822f247b5fe1577bd4d9c5e275cb4951799b75968c67717886cfa5b7e57e`  
		Last Modified: Wed, 17 Dec 2025 22:10:27 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d1cabbfb88ad65c8637c9245a85b0f127e99b55e0ee8ec9624bef5881da125`  
		Last Modified: Wed, 17 Dec 2025 23:10:44 GMT  
		Size: 3.4 MB (3419943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2971af748b4dd34696303854743547cf8ac64ed7d0476d7acd3bc02ca4032cc4`  
		Last Modified: Wed, 17 Dec 2025 23:10:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f43cf6f9164bdb156fe010f8449c1099050932f348906e82f79ea0ed63a959`  
		Last Modified: Wed, 17 Dec 2025 23:10:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499a07fa055232abe20e3ec9f345dc1ce1d90e2827ae526b3a0cccdf39cab87`  
		Last Modified: Wed, 17 Dec 2025 23:10:39 GMT  
		Size: 17.4 MB (17370982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8f019c760ac6d4552eea5f70b98efebc4426db7f639a7af982bf0a08c51ccd`  
		Last Modified: Wed, 17 Dec 2025 23:10:36 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:4b93f7bc8ae4556b50bc3afe28cc338ffb0eea7970c73ccdf9d35bbeff556b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb138dcdb16906efde95c25bed86d2873bf8547d8942e0a8a70f1cd2bafdf7a`

```dockerfile
```

-	Layers:
	-	`sha256:19846c9d010cc2763d6aad641c6be7c1040ec8b91c4e0581b2c3c74e487b1e0c`  
		Last Modified: Thu, 18 Dec 2025 00:08:04 GMT  
		Size: 30.3 KB (30341 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:29-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:3fb1949f917f2df22446aa3cbbac7a8be126df603c65beb3c85c6ecbf46400ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148650916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3752cbb9ce92ae4b893a33ab4b3952e7dd2639c5dbcd3b684baa9ce755251a25`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 21:56:59 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 17 Dec 2025 21:56:59 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 17 Dec 2025 21:57:00 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 17 Dec 2025 21:57:03 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Wed, 17 Dec 2025 21:57:03 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 17 Dec 2025 21:57:03 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 17 Dec 2025 21:57:04 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-amd64'; 			sha256='c37114fcd034025ec68e224657c8a5a850df472ded3ddcbca75ad3a7ebb9710d'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v6'; 			sha256='348d17c7cc881e9268255d6f404669ae29789003575d1da9d97b51cd6ca7f0dd'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm-v7'; 			sha256='32646cb57c43640a71c81f206897b78a8f1abe6b6db62bab115b5940fc5be884'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-arm64'; 			sha256='31d012d52d6df68aef4b55db62330967b562811f0de30cdfaa4505f314797c76'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-ppc64le'; 			sha256='13523e8d1820019f404df31c7ec17c7a76c16f638dd04acc33f5d141f683247c'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-riscv64'; 			sha256='86af30811ceaad9fc34a6bc02e5d093d1460ec24f125c47e639ed1fac9effe83'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.linux-s390x'; 			sha256='b752c6824bcc355b012d6f595987706fef15243792fe755f50de76c979bc592d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 17 Dec 2025 21:57:04 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 17 Dec 2025 21:57:05 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-x86_64'; 			sha256='5091bac5729ce968c602d157c2f0b959b7b367d4efb70aa864eb9ae78eebe13e'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv6'; 			sha256='119ba4f6e2b3b2deb8e8bc57fbc1a73c9197b34c4118770582eedc582c2c5ed6'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-armv7'; 			sha256='0feac2ca0dd33f40eebdbe8744b06eea2fe768c311b2fa3e29814b27ab832ccb'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-aarch64'; 			sha256='d68ba7053066a44a51ee33b7dcdc106d8c8745eb0eaf46dc59fbbeb22ec46392'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-ppc64le'; 			sha256='449dd11d3468dca4e1a33426cfebcd67dd097583ea4456b47878ccee907965b9'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-riscv64'; 			sha256='550938fcca6816dfe1b6ca10387f88860ac0f11f363ca39fa012d3d64364e479'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-linux-s390x'; 			sha256='0a291c1fb6887ce3a81005a9bef6b8e6c666f225d9b5e290cd564f9d19de6cc5'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 17 Dec 2025 21:57:05 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 17 Dec 2025 21:57:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 21:57:05 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 17 Dec 2025 21:57:05 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 17 Dec 2025 21:57:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Dec 2025 21:57:05 GMT
CMD ["sh"]
# Wed, 17 Dec 2025 22:10:27 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 17 Dec 2025 22:10:28 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 17 Dec 2025 22:10:28 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 17 Dec 2025 22:10:31 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-29.2.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-29.2.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 17 Dec 2025 22:10:31 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Wed, 17 Dec 2025 22:10:31 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 17 Dec 2025 22:10:31 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 17 Dec 2025 22:10:31 GMT
VOLUME [/var/lib/docker]
# Wed, 17 Dec 2025 22:10:31 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 17 Dec 2025 22:10:31 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 17 Dec 2025 22:10:31 GMT
CMD []
# Wed, 17 Dec 2025 23:09:57 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs slirp4netns # buildkit
# Wed, 17 Dec 2025 23:09:57 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 17 Dec 2025 23:09:57 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 17 Dec 2025 23:09:59 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-29.2.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 17 Dec 2025 23:09:59 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 17 Dec 2025 23:09:59 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 17 Dec 2025 23:09:59 GMT
USER rootless
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc093fcac0b21c8e4b147df323178d7d63970b55ee29c274491d945acc84bd3`  
		Last Modified: Wed, 17 Dec 2025 21:57:30 GMT  
		Size: 8.5 MB (8453513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03df120d22efa88ba94e13be34cc1e688af5eb25341c732001a4b0bcab5b09b4`  
		Last Modified: Wed, 17 Dec 2025 21:57:29 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768aeb4f03d334c6ec08d0c734ac8337b0973d7379dbbbf0b92f3376b92e146a`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 17.3 MB (17336619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e865c49329c3ae8a6b29c4d5b28e872519529032d07cd0e9cd3dd111da9b788e`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 20.6 MB (20645061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96ad87ba14e1729ac91d9fede405f1eebe237e7342dd1bf5bc0dfdb9d86a439`  
		Last Modified: Wed, 17 Dec 2025 21:57:31 GMT  
		Size: 9.9 MB (9938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871e4a9186fad94bc2536fc67abf7d8d69259f4b424fbeb3f7c5635357936722`  
		Last Modified: Wed, 17 Dec 2025 21:57:29 GMT  
		Size: 539.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3a1443a354124beaa10597a51eab06b6b40cc67d813d16c0f9b67b9b7907d`  
		Last Modified: Wed, 17 Dec 2025 21:57:29 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef2883fd7d374e9ca661a106c6602b3a8a36c81d354fa82a37de693f56b86b`  
		Last Modified: Wed, 17 Dec 2025 21:57:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf3be1176a851dbaf8324cba241250ab226bdd88b2fe9383ae16ecb60fcdf8`  
		Last Modified: Wed, 17 Dec 2025 22:10:59 GMT  
		Size: 7.2 MB (7212596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d6f2d4428530a64f1998389ad4a628d4350373e6b7d6ff9d707dd399599d0f`  
		Last Modified: Wed, 17 Dec 2025 22:10:58 GMT  
		Size: 101.3 KB (101262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764d70f457b46caab8c4cf071447bcec10f7e6722f219caa8e9fccae76ad0194`  
		Last Modified: Wed, 17 Dec 2025 22:10:58 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648ce6b9e925e64facec5a4c60786b717e529097d05ccd009b7771e64523a73b`  
		Last Modified: Wed, 17 Dec 2025 22:11:12 GMT  
		Size: 59.7 MB (59655377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62a0d9634169e77311ded04b835763839d00c0998b8b35b7defeae9408c9c8`  
		Last Modified: Wed, 17 Dec 2025 22:10:58 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d04c8a202df84690256b527936fa676d8ba90f4221dd379a57dfae4c0bf7dc`  
		Last Modified: Wed, 17 Dec 2025 22:10:58 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ba64de92c498d86b089a2f301899e493ee9c6ff9dddfbd1b99618654da08dc`  
		Last Modified: Wed, 17 Dec 2025 23:10:22 GMT  
		Size: 3.4 MB (3394369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370c6b580400e19ffa1ca9e598607931fce27dde70490ec3e893cb30fa25d762`  
		Last Modified: Wed, 17 Dec 2025 23:10:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438e735c75cc6a7c8dde0e140732ed69f54f70a03e3dc06f2753b05dc238d2c`  
		Last Modified: Wed, 17 Dec 2025 23:10:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf1243e7bdd701a3eaa9ca3540b90afd300a83a4052f61a122ff51cce2b7a39`  
		Last Modified: Wed, 17 Dec 2025 23:10:25 GMT  
		Size: 17.7 MB (17708722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d476ee4f3b6710956b3feaaa54e878fcac04ae92e8c813930e205b895355c2b`  
		Last Modified: Wed, 17 Dec 2025 23:10:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:29-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b0db54624a361f50b0898ed7a78e754db6bf6ba86b1150b1b01a215fca0c4e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b609d8e0174338f93439dbab60f629a57949f24335fbf5c077b12db78e9e28`

```dockerfile
```

-	Layers:
	-	`sha256:b6bba76181f445bb7e64c5a54b7d582e4447e3d39bbc37329432862bad3bada7`  
		Last Modified: Thu, 18 Dec 2025 00:08:07 GMT  
		Size: 30.5 KB (30492 bytes)  
		MIME: application/vnd.in-toto+json
