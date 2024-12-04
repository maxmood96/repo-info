## `docker:27-rc-dind-rootless`

```console
$ docker pull docker@sha256:8eaf4f3a2d19b7050827be83ef074a793d0d7a26799ae702f0e437dbe1723e96
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
$ docker pull docker@sha256:50faffd8afe18a7aef79b15f5525ca63ea705c8d0eb702a08ea9fec333fb0da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152205568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddbaf009efe732ea21c428046dbc4fb396fc834d44ffec7bb5386e2f9852df2`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed4036cbb7a2e5b8a0ce714e4d08fbb64576b80cdd256ff9f0cba6473d73c3d`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 8.0 MB (7998285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60d77d28745a9052470e2cbb96a13d33e0a0e02f2499098e3d150ae69df6ec1`  
		Last Modified: Wed, 04 Dec 2024 01:35:24 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308d551e66ecd4619442c0cba7f04c9163e61b0945a74ea8d1bfbb15fb71005b`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 17.6 MB (17618505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e5a50b00019a8a9b9d2ad27fefe556926cef90afc2e4767c403508f7a5f010`  
		Last Modified: Wed, 04 Dec 2024 01:35:25 GMT  
		Size: 17.1 MB (17094300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5f989342af03a88bce377b617864cece3f5ad629a22a51e2d34812695a173`  
		Last Modified: Wed, 04 Dec 2024 01:35:26 GMT  
		Size: 17.5 MB (17533135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf2ee14890d7b572c08a9fb8276b82863a29679e8332de749cca4310bb39096`  
		Last Modified: Wed, 04 Dec 2024 01:35:26 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01edf67849db938f70147e8d18b500aaf45f2bb8e5f32745257140f0d7a70bdd`  
		Last Modified: Wed, 04 Dec 2024 01:35:27 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1621c258342360b40a9cc7fd4ae6895854a32f239b97473f8477c201839e675e`  
		Last Modified: Wed, 04 Dec 2024 01:35:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f140d4d74a56b54fdd1a047b1fc2ee31876eb5308d3d81e3fedc780b34c3a7b`  
		Last Modified: Wed, 04 Dec 2024 05:06:17 GMT  
		Size: 9.9 MB (9854874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a366e43bf26c224272702af115fda4e51586c983c8c1ce67ae810b8492ab955`  
		Last Modified: Wed, 04 Dec 2024 05:06:16 GMT  
		Size: 98.7 KB (98664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae7cb273ef2e4461a34a8c37ab8c4b239eb937bc9e2837af3602b3e84e8c87`  
		Last Modified: Wed, 04 Dec 2024 05:06:16 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acbb54de8809a743bbc3b7cc0203480f0a2dabd96dc49d5b879282d65e87e45`  
		Last Modified: Wed, 04 Dec 2024 05:06:18 GMT  
		Size: 53.7 MB (53731404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ad16259f16861fcbd5e5f78133325a8820cbe074be078b01068653df7af2fd`  
		Last Modified: Wed, 04 Dec 2024 05:06:17 GMT  
		Size: 1.5 KB (1514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9e8f2c7de67ffb0101bd8d729fcdef868dff848fe115cd81e56f80fcf084af`  
		Last Modified: Wed, 04 Dec 2024 05:06:17 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52fe63ac34694e9860d1bc3681c03b455748f2c06646324eda121a267e9b8c2`  
		Last Modified: Wed, 04 Dec 2024 05:44:22 GMT  
		Size: 1.0 MB (1023839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd183b15b072af63a5f1e1d687dd6a2dfbdcf506f24daecfabac652fa05ff97`  
		Last Modified: Wed, 04 Dec 2024 05:44:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3da6b6552111e2513a0b21c9f63013ca8c20fca05da5a944ca7c9c9d9dd027`  
		Last Modified: Wed, 04 Dec 2024 05:44:22 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7086d5a3f109ba7f32544bf4e9df71177d15e20384bf0c98c63bf1fb9cf6a6`  
		Last Modified: Wed, 04 Dec 2024 05:44:23 GMT  
		Size: 23.2 MB (23155536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d66d8d7904dc2d346b71e8c5b7e0612bca68ba0ca6aa4ad0c70980ba19dfc92`  
		Last Modified: Wed, 04 Dec 2024 05:44:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:af9edc1c09f0563fa36806815e0f04d9fa26bee522aea838b86d64522458bd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87063df0e78ddd3bbf64849348fcb666630b29f1efedf1205eb35b1f3bb66dd`

```dockerfile
```

-	Layers:
	-	`sha256:923622d36c6d265d589391ddb51b549c0e45931476fbb1a42feeda227608eb7f`  
		Last Modified: Wed, 04 Dec 2024 05:44:21 GMT  
		Size: 30.5 KB (30527 bytes)  
		MIME: application/vnd.in-toto+json
