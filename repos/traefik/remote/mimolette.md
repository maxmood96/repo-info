## `traefik:mimolette`

```console
$ docker pull traefik@sha256:7c1cb803a546e3c94a2a71e26d35d8b4f24e844acbfc0b0d0e10b9938e8427dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:6c54edb4737f5d795c32e884ed9c4338335d8056e44316a1103de45859cef1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49198491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a644370b7973fd15708cd7f7f393fbb7c7f3bd2b28bf07a210ee1420bd769e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0861e679c547d11e7964205754a8e6d995cc0fed869e6023f116ffa0b1e3f`  
		Size: 461.8 KB (461801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e15fca152af0ef27efac381b94b2483c000c6364c291f3be064a6642e3f573`  
		Last Modified: Mon, 16 Dec 2024 17:29:21 GMT  
		Size: 45.1 MB (45091878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c32679c77cf46cce65c8878492a98155f11428251c4a14f38e6fdd930ee458`  
		Last Modified: Mon, 16 Dec 2024 17:29:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2ac1e0f6462b3efcd37a6c74291866320c0c308bcc89df32e4e341a4a449ec94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **829.9 KB (829892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4285ff33f0eb1cec239a976ca9fbe11accd86cb33ac1af114383a17cc69a0`

```dockerfile
```

-	Layers:
	-	`sha256:b0f3255e243f55e3e90947d53f7538ac18d2d8b3a59d80e7bc30e08e4d074fd5`  
		Last Modified: Mon, 16 Dec 2024 17:29:20 GMT  
		Size: 817.4 KB (817355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e0bb1a9ccec2a30e13b9e220d4dfcc121167cce609801c466ede75af87847e`  
		Last Modified: Mon, 16 Dec 2024 17:29:20 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8bacb5a4836a3a6e7df41ee0f5b25e9359b9acea3bbd8304d2944718c9ed4561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46230057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d0bee172e775fabb2173fafdc1fb98bd5a8a29f71b8b525ab7c4f2739708a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92901f08881e2db31f763999740c8205a808d7b994dc4c764e09e6b7bce069fc`  
		Last Modified: Tue, 10 Dec 2024 23:08:43 GMT  
		Size: 463.0 KB (462956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ff824be8c36f1c110d044dfeea6ed818febcba680a3d22735761f7cbb2a13c`  
		Last Modified: Mon, 16 Dec 2024 17:29:36 GMT  
		Size: 42.4 MB (42399550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c640250a0d0bdb8d68efc5a3fcdd6fcb2897f3aca97b7d0e8e83a8140e48478b`  
		Last Modified: Mon, 16 Dec 2024 17:29:34 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:e052f459628b6ba243acc512c181f46da5ce0f390e294f2bc5dc71307b7623a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483fa59d8441d9338bf44d8b39ea866d742cb8e995bceaf657ee7accd64617ac`

```dockerfile
```

-	Layers:
	-	`sha256:21d186a29621107b9c45660300eb34291cdbe56f6be7bf915f9be1ec183b00d7`  
		Last Modified: Mon, 16 Dec 2024 17:29:34 GMT  
		Size: 12.4 KB (12435 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e105e636a6d10eb1791ed9af4b125a9b55fefe9ea2220c3ef68f8f05708adf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46226279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7e5f07b7717fd8e573062a2467250632c2975a04877a66723094ffebbaee1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585859b3274a951bc36b95adc08606d5a5f9c3d34a636b612d2100b16ba19e52`  
		Last Modified: Tue, 10 Dec 2024 21:23:31 GMT  
		Size: 464.9 KB (464902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b352298bc210ea9a67dbc8eb3114c831562e294d446809c8dd3070e48933aa9d`  
		Last Modified: Mon, 16 Dec 2024 17:30:33 GMT  
		Size: 41.8 MB (41767822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bab574536e4d7e9d09468d1a47e352a272fe9a5a7b1369d28eaed25ee5496b6`  
		Last Modified: Mon, 16 Dec 2024 17:30:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:609f3a687085d31352cb58c3784cd89f252bef276645f7cd41b4f8b6561ecc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **830.1 KB (830140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d526dded1650d668b39399ea2b773a4b970983fe0759673040c5db6ce6af373f`

```dockerfile
```

-	Layers:
	-	`sha256:6c4e7a29eee9c1f73dbd51959ccd2c1aae72cb92cceacff69f47810e2f223724`  
		Last Modified: Mon, 16 Dec 2024 17:30:32 GMT  
		Size: 817.4 KB (817447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c770a4cb017715cff2fd2542330aae04887b6a69452b3221bb448e113fac07`  
		Last Modified: Mon, 16 Dec 2024 17:30:32 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:e939d699e6a3faec70fc92de20738736b0039313dd1a04c19f98932e853bb235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44641802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3939fcc2825b84762b7369a8bf30487ae1cf857c000044a1915b898510f7799e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b179457363cf87dfdcdef35a6cfec4e16b8186a6012d35c4dd8f272c1c3e2c5`  
		Last Modified: Tue, 10 Dec 2024 20:27:34 GMT  
		Size: 465.4 KB (465356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205a7e394b8cb767b675268d58e99c62f522040284d5e29412c9e2a56f486bb0`  
		Last Modified: Mon, 16 Dec 2024 17:31:26 GMT  
		Size: 40.6 MB (40598969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378a1913d8cfdde38327c187c34e2aa053c7571f37c4f1ca3fba71b82a81b8bf`  
		Last Modified: Mon, 16 Dec 2024 17:31:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:8c2b2e38fe1e9159a38a08d781c25c1c008843e0376d5f315730f2e719bd11ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.1 KB (828055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b48fca611985d85552c0799072b09f9e17c79a2174d366ad65e383153f765`

```dockerfile
```

-	Layers:
	-	`sha256:875228d49bf5fc48863c67c3d253e71ed25cb926481ef2435c03dbc25d6a0100`  
		Last Modified: Mon, 16 Dec 2024 17:31:25 GMT  
		Size: 815.5 KB (815453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da9ae5210adc86561c91ad773a344cedfdc1393f7f49d3bce6482ba464033f27`  
		Last Modified: Mon, 16 Dec 2024 17:31:24 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:2bea9d63097be1e6271cfcc4d2dd0876fc2cd4349eb14bb9a1cf731489adc5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47519755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6d774b18fd554deafd99e27a16f88647830fe6b09b400224cac612be6bf4da`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9864328760025978421ee21682a648061ab9574b8a21ad93338990a16f5f27`  
		Last Modified: Tue, 10 Dec 2024 20:33:20 GMT  
		Size: 462.0 KB (462035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70be148a9da672dc4cfe3bbb76cb7bc208e239f4b3a1cd7f9b80074abf60e02d`  
		Last Modified: Mon, 16 Dec 2024 17:46:41 GMT  
		Size: 43.7 MB (43703329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f47039c8d2282274fcf905da4e2c0093263fb049e17fa4e33e505d640e1cb1`  
		Last Modified: Mon, 16 Dec 2024 17:46:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:4066af35af00e6ca7eaa2650680d9e0ff0595b4b748a62a9a19ea31e46920e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.1 KB (828051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2c0752b1ba27c920ebd99ac2bb093c4f4880c8ab073dbb33bd04164a9950b2`

```dockerfile
```

-	Layers:
	-	`sha256:a1d0707a23c95d9656a18ddd262af88de1483626ef89a23cc07bc8f2f1eec2f9`  
		Size: 815.4 KB (815449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc5d3c9aeb8c6356576bf4f4a7916f69f2ec14fd8bd5834a5865a1f35abfc71`  
		Last Modified: Mon, 16 Dec 2024 17:46:35 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:71b36071b7840bd21f84819038f585e12cdfe231891afb6505863c45d58e3735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47939573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ce63c89264790d0a963c8bf33a69de281a447a3b00e38c9222e807bd99df8d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.16/traefik_v2.11.16_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Dec 2024 10:01:22 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Dec 2024 10:01:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Dec 2024 10:01:22 GMT
CMD ["traefik"]
# Mon, 16 Dec 2024 10:01:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.16 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb6169870253f9ab8474b704a4354969efb86461ccf96e01c840e72f9d0bdf5`  
		Last Modified: Tue, 10 Dec 2024 21:11:13 GMT  
		Size: 462.9 KB (462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9652b3f55852376130ff8e6386d51ead4b3454323873fe11f6fb7463025b2d3`  
		Last Modified: Mon, 16 Dec 2024 17:36:55 GMT  
		Size: 44.0 MB (44006817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a929ef51550773e7bb31c924c8b02f6761744fdcb74b436d61e525014ba60`  
		Last Modified: Mon, 16 Dec 2024 17:36:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:11ef7301c041596dcac0c6c8a986199bd1e54f15f9d3d1a864354ea4a4f0a1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 KB (827935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4add08fab06170b18881ca5e760d19dfc273187cccaa2a92ccd986e78be76ce`

```dockerfile
```

-	Layers:
	-	`sha256:388163df71fd3a29d651ef622865def2228cd2859ad80c59fd3a564fb99fdf62`  
		Last Modified: Mon, 16 Dec 2024 17:36:54 GMT  
		Size: 815.4 KB (815397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f592b81878326a303bff3ab6a6e73bc33f683110180e73b7b3b75e0ae6bdf59`  
		Last Modified: Mon, 16 Dec 2024 17:36:54 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json
