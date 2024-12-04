## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:7e089b525e1a32f58f70ddd85bcf5b3b17166c6192a0e986824cbbb0a9b64d02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:40a939688f7acdd08ac63d801cea18c4ab65a845fb20d12333c8c3a81d89d3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157768550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb90aef007fafd734c7a398efbe32842c2789cefd0e2b065ced02c3846b4909`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:22:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENV DOCKER_VERSION=27.4.0-rc.3
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 03 Dec 2024 22:22:58 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 22:22:58 GMT
CMD ["sh"]
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
VOLUME [/var/lib/docker]
# Tue, 03 Dec 2024 22:22:58 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 03 Dec 2024 22:22:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 03 Dec 2024 22:22:58 GMT
CMD []
# Tue, 03 Dec 2024 22:22:58 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 03 Dec 2024 22:22:58 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 03 Dec 2024 22:22:58 GMT
USER rootless
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b85903ec8b1df840360cd2151154fdb9e3b95289511c9fc6021b0495ad50b3`  
		Last Modified: Wed, 04 Dec 2024 00:29:22 GMT  
		Size: 7.9 MB (7889983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f192341fe327337766a6ebeea88b150b7c6e47959f2dd821d2a71eee1966fc`  
		Last Modified: Wed, 04 Dec 2024 00:29:22 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0298a17636a9996e9be91870cc0464cdeade82bda8c0311398e2570a68268eb`  
		Last Modified: Wed, 04 Dec 2024 00:29:23 GMT  
		Size: 18.7 MB (18670373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef88d56d23169eb0baa939f61bd17754f02fc95d4b4798a52d4872ca6697a73`  
		Last Modified: Wed, 04 Dec 2024 00:29:23 GMT  
		Size: 18.8 MB (18797153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e7954e4d65e51a1c462c54caac06400b6606d29005c715ed4a7ea6976d3dd`  
		Last Modified: Wed, 04 Dec 2024 00:29:24 GMT  
		Size: 19.2 MB (19188663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e603e8c59a20d8770028eebdff1efe926f1b9d15195ed3d313262fb7bd4f8ce4`  
		Last Modified: Wed, 04 Dec 2024 00:29:24 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6905ff1e515ac5aa91c9d027f49010e525cbff68fc73516f5220296cc7b44a89`  
		Last Modified: Wed, 04 Dec 2024 00:29:24 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc1cf61c3682743407fe4fe72a0245ff7c5b6a78603495da07de2328b30383d`  
		Last Modified: Wed, 04 Dec 2024 00:29:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b166cab208d58fbbbe2a0f2cff4b2b81831a3174af31d1b39de35edc5d500e80`  
		Last Modified: Wed, 04 Dec 2024 01:28:41 GMT  
		Size: 9.1 MB (9067204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9cbf91bcf3a1ab1a19585220981064a8e4c7a6c1967c47a1ab534e1f6940e3`  
		Last Modified: Wed, 04 Dec 2024 01:28:41 GMT  
		Size: 89.2 KB (89234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed66722f7a967d1278a22c81086e2097d094cc730db3fc8a53f3d6fcd86ffb0`  
		Last Modified: Wed, 04 Dec 2024 01:28:41 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22fc1d56bda96c8f592661ecacf4806c8cc4c1f113211d2bfdb2a3a6048b32f`  
		Last Modified: Wed, 04 Dec 2024 01:28:43 GMT  
		Size: 58.1 MB (58147902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d791efc729932966c49670cd491b2ae0cbf7c7b041baae42f234953501ec4813`  
		Last Modified: Wed, 04 Dec 2024 01:28:42 GMT  
		Size: 1.5 KB (1513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc125db44f7c35b94232875d75064ff7b8c17cc98ab383d88ab234f3c1c7ec0`  
		Last Modified: Wed, 04 Dec 2024 01:28:42 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1845476d58be30b89c42879710ec65ab787461b35e427055fe1f19e70215936a`  
		Last Modified: Wed, 04 Dec 2024 03:07:41 GMT  
		Size: 981.6 KB (981579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e82fc1394d6b14707ccffaaea8f7cf22b75d41d7864f597484b4f430ae13c8`  
		Last Modified: Wed, 04 Dec 2024 03:07:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2a8ab914a1c57ef8cad627a467073af4bdaefaef233ab2c52190079b77bb2e`  
		Last Modified: Wed, 04 Dec 2024 03:07:41 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8d0f0f71e648cf29cb49ef7d6a7996a5acd8eb588a7748a0bb7b05e3129702`  
		Last Modified: Wed, 04 Dec 2024 03:07:42 GMT  
		Size: 21.3 MB (21303252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc145040997f5da3ab975feefec5033a807775487ff46325107c34bee0c91053`  
		Last Modified: Wed, 04 Dec 2024 03:07:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:08e9a10ad7b34830bb95363da612b1a47e69e4f1fad212290d7d518a48bb7025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1b1af3e7c67b49d29cec89f209b0cee1cd5c9856cfba9f549a7d4a1d909ffc`

```dockerfile
```

-	Layers:
	-	`sha256:bf97b39a5de058be7ecd5c97b175b39d84670dc88d7fe8a445a5ca3594bc39b5`  
		Last Modified: Wed, 04 Dec 2024 03:07:40 GMT  
		Size: 30.4 KB (30370 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:4e707f345ee1ee121db45d139bda698101dbc0fa8d88885a36037d5bae0d4d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151866576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e99cc8f8669c7de9d291a3321fd97410d71a0a193aeed8a512c8f10f00ca46`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_VERSION=27.4.0-rc.2
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-amd64'; 			sha256='4fe2eb90ac22b27fa03734899fcf814aa1e214a4952b9b30b20d551baf1d9a5c'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v6'; 			sha256='f438c1845f515b7deda0d7f325752f5652f2206a34ab2fff611f8a8717fb8907'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm-v7'; 			sha256='606e449ac112615e0bffe6c433e59e84145e6963119ea397227381b86da3a880'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-arm64'; 			sha256='da9742321bb462547ebde69bf8420ac07b2a2c80fb57260f539bfc9f312becd6'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-ppc64le'; 			sha256='ef63b95d022c53b41b2404aef7ca77c2e775f2be63566d2af00260ed13c51984'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-riscv64'; 			sha256='49dd68603c992b6755fc7c8a7762fbbe689f2aca97a55a513c978e02582f9a81'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.linux-s390x'; 			sha256='f4a69adac9a2734ab191c29529f54012b289884b626d75baa3cf0471b0241f58'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64'; 			sha256='fbb4853d3f2148b0f2f0916f8971c9e500784e4e4949324934fc0b7dc2ed5016'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv6'; 			sha256='7116c73bd22504ff61e5e25f3ea6638a7b2a5d126764fccdec4fd7623cf17963'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-armv7'; 			sha256='944402b85b5eb8492ebbe2e4dcbf962adcaaa16b0ed66b51abaf2ac3e3809b1b'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-aarch64'; 			sha256='8fed7b79b8bd1cb0624142f7d723c3cc67ba747c77ed69abbdefdc77a6d416d1'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-ppc64le'; 			sha256='9a5d9fd85e852a9c3c9137ea8ea80d66f0fe349d34b3e329255d98cd960c331e'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-riscv64'; 			sha256='eda617db72d24fe79be98e2273e1fb433943a18479cedc86601963f75666304f'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-s390x'; 			sha256='9476a64e9605df956e3e33b09acfdaed2d4a2c71da5b4a09899a9b7d428263a0'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD ["sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.2.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.2.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/var/lib/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Tue, 19 Nov 2024 18:04:23 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 19 Nov 2024 18:04:23 GMT
CMD []
# Tue, 19 Nov 2024 18:04:23 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-27.4.0-rc.2.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Tue, 19 Nov 2024 18:04:23 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 19 Nov 2024 18:04:23 GMT
USER rootless
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c2943fcc4c049fb6a537793b27e1f49f7fbf03dccba1f916dffc11bf201c22`  
		Last Modified: Wed, 20 Nov 2024 00:24:42 GMT  
		Size: 8.0 MB (7998165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb19f166db867e8841734ae49cc6de3ff5e775f528caefeca64e45c74d72a75`  
		Last Modified: Wed, 20 Nov 2024 00:24:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7399e06c10a10d4b2338d3e8f5a1d38337678a02b582214d7cce00efde54c83`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 17.6 MB (17619942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a2fdee375f19d800d1c3b9f7eb17d6333c9e65fedf1839b41f0b736282d9fd`  
		Last Modified: Wed, 20 Nov 2024 00:24:42 GMT  
		Size: 16.9 MB (16905174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa5086a97056f2dd54bf2822cbb50efeb702abe4c58e6cc7b2bbea7084d2b4e`  
		Last Modified: Wed, 20 Nov 2024 00:24:43 GMT  
		Size: 17.5 MB (17489942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63283e47922e1addd6aefeb0a95800495d23942e877fec9bd8c3b0cbc072a6de`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 540.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8439390d1e56e7c03233d875d55345d5b0a70be6a0423c5d923cc02ac86dc7`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf0388e567e31b4ae89d097b0d536a143ef34bcadd4804ff36d7940849e286`  
		Last Modified: Wed, 20 Nov 2024 00:24:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1947b4c47fb16179408481f4eb141f1e24c412f05704adb0ce8fe12c69a85b28`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 9.9 MB (9854532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccbd1e5df7e13468530d95f6a2037740bfdc85421620aee47b70f9e6f49f3c7`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 98.7 KB (98660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49fd2d46af5d4b6baaeeb50693a9e720ace3763f4f879abab41e826b1f2108a`  
		Last Modified: Wed, 20 Nov 2024 01:07:25 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d56ff2075a0e0f65dc9196b76485511d627bdc80fe6b9788b3780cd89895789`  
		Last Modified: Wed, 20 Nov 2024 01:07:27 GMT  
		Size: 53.6 MB (53623757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd38104c887c5ca084596f9434e6ea5eecc44566ac9b99bbbc9b3ffd1d68ae8`  
		Last Modified: Wed, 20 Nov 2024 01:07:26 GMT  
		Size: 1.5 KB (1511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1774b93662bd3705c185b3859d59d836046419f3c63c035346f9d5323d0db5e`  
		Last Modified: Wed, 20 Nov 2024 01:07:27 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57c0c1f17806e05dc826939abe479e0a49215c5bd114f5f3f1263d5e5db5be`  
		Last Modified: Wed, 20 Nov 2024 02:07:26 GMT  
		Size: 1.0 MB (1023832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8f7b7512fe668da279f450a1fbc3bfa7152869850f79e82f7ab5e37da81223`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe4d3f949cb427b4b1c2e57da68eb3f7190a0d14cb535a745e3439816249af7`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c36e404f6851976c8ecc58c5419cb6d277ba16128d31e751eba47faa9a3208e`  
		Last Modified: Wed, 20 Nov 2024 02:07:27 GMT  
		Size: 23.2 MB (23155543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08452e49379ff4821308a12bbd57db262fda64bdc86dd9138424fc28452c005e`  
		Last Modified: Wed, 20 Nov 2024 02:07:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b4b920fea6c15c5e5a8094778376f1be3004d69a8ccc42eddd8bcee34eef155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba1e1825ffe9f950747487ef0d48af747bc2491a282bea23b30a79204355f9c`

```dockerfile
```

-	Layers:
	-	`sha256:c6a53381b16d3917ee9ca7dc394c638d0fd7f56d135a3988d3e4e48d911435d6`  
		Last Modified: Wed, 20 Nov 2024 02:07:25 GMT  
		Size: 30.5 KB (30526 bytes)  
		MIME: application/vnd.in-toto+json
