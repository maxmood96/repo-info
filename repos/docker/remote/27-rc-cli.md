## `docker:27-rc-cli`

```console
$ docker pull docker@sha256:89582140f7c16f8dac6c7da090f30cd024e423060561a20c5d2eda4bd947a6e8
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

### `docker:27-rc-cli` - linux; amd64

```console
$ docker pull docker@sha256:186bc2ea1fab46dc414d517e1a03e2a527a0063d64c79681d06a9d394d097fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68171944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f37ac682a068f30a3f56223163ce221c2586f9ec037eca08a3a594cf5882de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd21b15bbd4f1eec87b8472942d7938153c089164bf5a69c0e0856154295575`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 7.9 MB (7889984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730abdaa54c4b34e02331e1049be567fcafc7a055a03973cc006af52860046bc`  
		Last Modified: Thu, 05 Dec 2024 01:27:31 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9998d48cc26c147898ed7fc62864176c6510e92cb6bc77fab0ee798f8ce4d`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 18.7 MB (18670112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d90d7f6b820c0d42567fb5fd6473c7e02bb259c3d42a1918d576dc2d8b99bdc`  
		Last Modified: Thu, 05 Dec 2024 01:27:32 GMT  
		Size: 18.8 MB (18797145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9388af133ec6cd03b483f9e4b68d054afe9aa4ff81fe6afc5f228395c79699`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 19.2 MB (19188652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0a0a9ba85388ad317ebab206be49bd4215c2168683babbad003dff85ca1770`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e3eec59449a506a400d58f5222ae31fb77ea13cd357d42a167a6faaf5f055`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b55d95c50d8573ea047a7480a6253b94d290ad4914d5cdc27689d38d9b3166`  
		Last Modified: Thu, 05 Dec 2024 01:27:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:076a3d163f2f971188f9b1cb9a73bcb29d989f4bcab03e5718b40443e2cdd0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55baa4bcdde520e651452e2bff17c2a4722e1015735acb39d48b6ab6713f4253`

```dockerfile
```

-	Layers:
	-	`sha256:6a1b28bc96a83326da6d57e1ee143f2569a9d64f37852bdc93e77f50b1204431`  
		Last Modified: Thu, 05 Dec 2024 01:27:31 GMT  
		Size: 37.9 KB (37911 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:b37ebe864a9389a4f08f96a415bbb264c3ad20b128308b210d91ac00184d1684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63342715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089d62964249f0bdc6b7646994a5f37b1d7998057b6ed5b6eec2801b62a7711a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28dec1f3e06da3f8757b7ab0c912b2790b19463c9e38b2e62db7016713ec835a`  
		Last Modified: Tue, 12 Nov 2024 02:19:21 GMT  
		Size: 7.8 MB (7820557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de83cdff8ecb35d376bef426a487ec59cb3c6e47646a152914957e84298f0d`  
		Last Modified: Tue, 12 Nov 2024 02:19:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c3a7cf2c8df780770d49966eb2d60e8c94fb8d5d17ad4c79b194cdb40bbd5`  
		Last Modified: Thu, 05 Dec 2024 01:27:40 GMT  
		Size: 16.7 MB (16706291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee1c787f2a41939b8bb36405a48560a5ffe591ddc9c624bb90515bed5fe328`  
		Last Modified: Thu, 05 Dec 2024 01:27:40 GMT  
		Size: 17.4 MB (17446676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367af08ebe91dce13d3eb6105c3d0418f5a5080a21b6c78d6279ce8f77b033bf`  
		Last Modified: Thu, 05 Dec 2024 01:27:40 GMT  
		Size: 18.0 MB (18000432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb600237c61b1a049107cf06e9d1dcf042380dc5c0a60a764077d70e9d22b4`  
		Last Modified: Thu, 05 Dec 2024 01:27:39 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbca203193471218e3f9f5e17fd03f9c5522a65a6674c83df985f5b062cdddc`  
		Last Modified: Thu, 05 Dec 2024 01:27:40 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f90b05a4d3d8c8bd6051c147b0a2150884e5d71fb004fe3a2a5a83f025f28c`  
		Last Modified: Thu, 05 Dec 2024 01:27:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:2d8d276b5d1fe9737acdf6c2e5744a3986d99e294bb1cb2c191a372ec0731b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4d8533ed9b93af7c347aa575d1d5d53eded83baf632374589ac7143801b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:d1e509066691fdbce3939711e972d1337e089275ce5e00f02c76287760287f48`  
		Last Modified: Thu, 05 Dec 2024 01:27:39 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:27162b5b50828c744c8602d1ae965789c113fc651d431bd0718700636c4b1fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62356199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3165433c9044609178a4951d35602519803e2a1c0a493368a1b20786aabbeb77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a8d373266083cffcbf2a6623223d8b2c780180ffc25c641834fa0f399b861c`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 7.2 MB (7153539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ecea7f1649dbef369192500f3eda21b1f30ba448ca4b382f6dc90ba4b77ed6`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704afe42ffd49fe0dfccaad3a9f7b82f5f421bca93b396eaa7c075d6d3ebc06`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 16.7 MB (16693980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089f77e5984ff6ae5fd9c58d78a3eecf9db758564fb7ebc929dcd8ee6f276b83`  
		Last Modified: Wed, 04 Dec 2024 07:15:41 GMT  
		Size: 17.4 MB (17426319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267680a19402b562d04ef49a6589872ab4fa787138565ad1e58c1ba391d3b685`  
		Last Modified: Wed, 04 Dec 2024 07:15:42 GMT  
		Size: 18.0 MB (17984726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953388bcfb6b3ba6e53e21d5ea4b90c33a41ce4dbd5bd8ee15fe9bc7159e462e`  
		Last Modified: Wed, 04 Dec 2024 07:15:42 GMT  
		Size: 535.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be4dab4b2a8971fce0674b700ab76798befa79ff842e093bc1c6dfccce7ac0`  
		Last Modified: Wed, 04 Dec 2024 07:15:42 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e590dbebc0c571e5838e8699e883700864e6a0c7973f637d93f7b2b5f8adc42`  
		Last Modified: Wed, 04 Dec 2024 07:15:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:c9d73854a1f29358a44779b783f99e1cb480a2976bc55ad941a777da27e854d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8675bd065ce83a3e3a9a84a187ad9bbd59c673698fd4cb09281ac3056eb84cd3`

```dockerfile
```

-	Layers:
	-	`sha256:f1f4030558523eab5380dff71bb9b87f21d3e643503a2ab191e7c896fab94828`  
		Last Modified: Wed, 04 Dec 2024 07:15:40 GMT  
		Size: 38.1 KB (38065 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-rc-cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:e38c568cf22245e2951dd094d508336b7f9f195f0263791570610a3de19bc21d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64334845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a33bc77cf60a8a40a07f1448bbb811736800fd7603750e69c4cef72dcc7f8be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-27.4.0-rc.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-27.4.0-rc.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-27.4.0-rc.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-27.4.0-rc.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-amd64'; 			sha256='153eace3d30c9efe9a7b94ea06c9d15ace59c8e6268d3481b8c175bd3df020f9'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v6'; 			sha256='6f7e15248535bcae3730444bbf6164d076b9df7491b89040153f12d9e93a9f6b'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm-v7'; 			sha256='b2bb531e4f217c94951173a9e403002f6b18868227f09715c295a63f837cf5e4'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-arm64'; 			sha256='9ecffda0a356957827de6b4ed86b151b420e84f81b2a58e2e2735506336ab891'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-ppc64le'; 			sha256='10ab6f3effac50e4150a3288013ad34e3cf4a0b307c7ffbf48dda9a5813e1bda'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-riscv64'; 			sha256='c89af9a424a109abd52205544377a9eac6027bb91c2fbe91d02cf91a6b53f7e8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.linux-s390x'; 			sha256='cfaf3883fe66787297c8df69e25f95246a74d630b5e2b6627cc563246f94b4f9'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Wed, 04 Dec 2024 23:15:41 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-x86_64'; 			sha256='8b5d2cb358427e654ada217cfdfedc00c4273f7a8ee07f27003a18d15461b6cd'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv6'; 			sha256='5812e2fe5e8fdbaa984679ad5809779a0a0f054a423a63f6d15167b5d643db43'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-armv7'; 			sha256='f8271667b0b0337cdd11a0f2920089f09b06bb4e5e3988e66ab23b5d18c3fa18'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-aarch64'; 			sha256='a1f85584584d0c3c489f31f015c97eb543f1f0949fdc5ce3ded88c05a5188729'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-ppc64le'; 			sha256='0f6149bb38f1722dea511fc80228d9bc7c3504cedaf662e09033d3aa89c70d93'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-riscv64'; 			sha256='f3f9a94dc4bb8773bdcd70680a177171e8aeb15b98b979fe51b447a5c97c52d1'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-linux-s390x'; 			sha256='6635a146193c797ed11ba3a6e9d7b1da5df0f1215ccd3c52f712001e58413f20'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 04 Dec 2024 23:15:41 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 04 Dec 2024 23:15:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Dec 2024 23:15:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a009e17f4dc05dabee0d38a9f3e3255fe4e8a9678f58c7a159fc2c2ca77a4d`  
		Last Modified: Thu, 05 Dec 2024 01:27:21 GMT  
		Size: 8.0 MB (7998249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1595925a5a90fcfa4f940a135fb5e1db4120b731667b85133d5bdb28898e034`  
		Last Modified: Thu, 05 Dec 2024 01:27:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1af072d56227d8b1b7ae55b503b511312941f2bd1c463de55ee805f1b2f5531`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 17.6 MB (17619258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b40c3a1432393d6915caa5950700e728cb6dc40aa3844e5666a495fc26387b`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 17.1 MB (17094311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d83bb451ed8682bdfa162bc305e29f07855bd243c332d2ccecb7867ce1a884`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 17.5 MB (17533147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ceb2e075ab6e99f2ed7470ae3b098f28507369156b4def4bfbef699e9052828`  
		Last Modified: Thu, 05 Dec 2024 01:27:22 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d05d15cafcc32afc225db5e5208c0475274e060392abeb5a5c2affbc78fb0a9`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23081dbeded38a453bb4cfad87df7eb60cb858cf380773b2b9fc2d79c68747`  
		Last Modified: Thu, 05 Dec 2024 01:27:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-rc-cli` - unknown; unknown

```console
$ docker pull docker@sha256:ae61ca5daf641c97fd64da6130b8c9eb2fd608fc40b30e49a69bc396b2260a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea66792803c35579df3fdeb763e6dba073ae901ea5bd549a864d84524dc0d3a`

```dockerfile
```

-	Layers:
	-	`sha256:5f669d0696720ca4bcb90fe4cbbb37f9d9a1ca3ab39990e0aca3f0cdadf83634`  
		Last Modified: Thu, 05 Dec 2024 01:27:21 GMT  
		Size: 38.1 KB (38105 bytes)  
		MIME: application/vnd.in-toto+json
