## `traefik:saintnectaire`

```console
$ docker pull traefik@sha256:bc534d72121b187efc3706780d604b2a6590ef321c441ef137289052633d27d4
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

### `traefik:saintnectaire` - linux; amd64

```console
$ docker pull traefik@sha256:8f3b0ac0ba29306f6d02f504b287ced562ed97c428c8364cf52a3a4dfa478272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52301448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018d945844efc555ba7a61a9140c94263c46592e8770bd8e9f3f6e1a567696ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 06 Jan 2025 11:18:42 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097e96f533aa17780d419807bb64f9e5997ec61c66cd02923d56bd6de2cdb646`  
		Last Modified: Tue, 07 Jan 2025 03:16:09 GMT  
		Size: 444.2 KB (444178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbf527ebf21fbfc408b403872e7cebc7a234304a4280f3721740695ae967d0b`  
		Last Modified: Tue, 07 Jan 2025 03:16:11 GMT  
		Size: 48.2 MB (48220679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c491c0965e86b20bc73df3977179e58e7e293b1b984031e41a4756c488d2424`  
		Last Modified: Tue, 07 Jan 2025 03:16:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:fa53cd97acb8baf4b6dc17551c4376abd1ff244308ad76c916e98d4ab4391fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **829.5 KB (829530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9a6278e5f215db6f66ed17c91670ab58a2e0dd26b147176a3074a85805103e`

```dockerfile
```

-	Layers:
	-	`sha256:0ff7f7718b5bfa6bb346cacbdeb5f5d3b2f7da2fb5fdab763c69e388554b6187`  
		Last Modified: Tue, 07 Jan 2025 03:16:09 GMT  
		Size: 816.7 KB (816711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823808a9d60173abf622d89766ebe823b190e58e37a7e7e08583736e6344f168`  
		Last Modified: Tue, 07 Jan 2025 03:16:09 GMT  
		Size: 12.8 KB (12819 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ea13d9a8a963210187b303066f75ff174e3cc9e4e6148ab96e72aabae0fab2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48903792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36266d176241f18ea5b53f7d469f2fc562165c323f29c788e1fc067200a1215`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 06 Jan 2025 11:18:42 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9da04419bb717369d836d223b6029bff4aff90bd4df3cf62e689d5d4f68ce2`  
		Last Modified: Tue, 07 Jan 2025 06:43:07 GMT  
		Size: 445.0 KB (445043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c6b91bc9770b9391ebe74ca15fd5a6a5fcfc6d14cf10d5e68350caf1948f67`  
		Last Modified: Tue, 07 Jan 2025 06:43:09 GMT  
		Size: 45.1 MB (45097346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df59b3ba8dfcb39af908d26890650f31d4b52e4919d7eb86c1433c8c8c83642`  
		Last Modified: Mon, 06 Jan 2025 15:26:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:2105a657813692bd530203fd6942752e478bfdd0070cf04f14703c44b795f123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36f230cac878ce9dc2e58d8fe96dd68cbc10d4cc9ac26d0176059b4be45e024`

```dockerfile
```

-	Layers:
	-	`sha256:648bf6cb79c28d17f3fdd6c5882e6873b04cfcd7684f4f2087912c1671ece1d0`  
		Last Modified: Tue, 07 Jan 2025 06:43:07 GMT  
		Size: 12.7 KB (12725 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:d2a68398c09a6234086c2b06cf9ec97110bff2277a4ef253b2e81d1c8f712f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49143355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47491f3b01ad25d079c6cdce52797b5a889131576413767001f7cd85b8efed70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 06 Jan 2025 11:18:42 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d015e3c2dc87808956c0341ec020c68713940a8a1c2d77f3a88fccb69544a`  
		Last Modified: Tue, 07 Jan 2025 07:10:13 GMT  
		Size: 446.4 KB (446381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ade484e2908e5659f6e90fc37a30a4f5bf2e4fa83fcc1305ee8b4be42c3ea4e`  
		Last Modified: Tue, 07 Jan 2025 07:10:14 GMT  
		Size: 44.7 MB (44713598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2475b0f262df46b2f79cdc1c4b441c6dc5bcfa506fdee795be8cd7b993e5486`  
		Last Modified: Tue, 07 Jan 2025 07:10:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:501fadeee86013a80a2cba4afd02b7db8bb3a88d294f97040b6428408b93878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **829.8 KB (829801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e635c8fed5c1bc2c66f9fe74f38107df5283cc8b7f4c0f31d02e7dda2a148`

```dockerfile
```

-	Layers:
	-	`sha256:edad64693608484448044a840707f356f0ddbcd90f9fdc98b9f5e1184c48c036`  
		Last Modified: Tue, 07 Jan 2025 07:10:13 GMT  
		Size: 816.8 KB (816815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b00adc6ab3fca30976fdcc22e7aa7756c4172e6d4aa52c8eda12de256ac9a2`  
		Last Modified: Tue, 07 Jan 2025 07:10:13 GMT  
		Size: 13.0 KB (12986 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; ppc64le

```console
$ docker pull traefik@sha256:0738284437bf9e2d23d6b0532ab9285aca3ab5ae183acf1ff5d94848d9c6ff72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47167453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719dca13612d2154309dc754a75e0213137def9becfc3e6a8f49aff9e60341a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 06 Jan 2025 11:18:42 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9a65fb645c1f955293754baab244e2409677c8d202e93738ef98008feb33f3`  
		Last Modified: Tue, 07 Jan 2025 06:14:47 GMT  
		Size: 446.8 KB (446761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e18197efb3de07dbec4cc03f6a109f369d06bdec0587244f23d1d0bc765854`  
		Last Modified: Tue, 07 Jan 2025 06:14:48 GMT  
		Size: 43.2 MB (43152578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73646fbf0694544cf0d91a11bd0116a03b396b31ebb74edf32ee159f60a8a806`  
		Last Modified: Tue, 07 Jan 2025 06:14:46 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:28bee00a6152fb505f78ca668097ebaedd8132a5a08d3f1d72320390d07b0343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.7 KB (827707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b19d4f3b9d6f11ffc128d1ec76693fb90c28b040e0e45341ea4cff6e3a8c0f`

```dockerfile
```

-	Layers:
	-	`sha256:01e531f72023c0e11fa9d95908e2457cbe51f2b82d24eee444ae57cbf4ae8dfb`  
		Last Modified: Tue, 07 Jan 2025 06:14:47 GMT  
		Size: 814.8 KB (814818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ad8dac851bcc82d6c9164b201e90bb091c668cb34fe2ab5fb2254857cfc7ee`  
		Last Modified: Tue, 07 Jan 2025 06:14:46 GMT  
		Size: 12.9 KB (12889 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; riscv64

```console
$ docker pull traefik@sha256:12a36599efe7d73b3542c181a34c75e08461ec94677f6facc268ca9aa4ed9e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50261914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd97115db2878e03f3261b2491f6898cfea1c8a94321cc3dfa038b1e3e99125`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:190d091eecf25aa983a0c39827a373152190b18fa399875539dc021a91c051be`  
		Last Modified: Mon, 06 Jan 2025 15:32:24 GMT  
		Size: 46.4 MB (46445488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541871784da833353211e5d73ac9e0228dc5303eea23e9387674ba418852c65`  
		Last Modified: Mon, 06 Jan 2025 15:32:17 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:2a060d52ac2300de0a295651b3a9f319442ce876aadef8af4360478147d2ae31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **834.9 KB (834903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db329dcbb3013d4ce232f05cf907c359361cb2a1c506b44bcb2ebbfb44447404`

```dockerfile
```

-	Layers:
	-	`sha256:6cd830809fb5176d35a36ab9350b937b8775a14ffc73cb8964843b034aaa5522`  
		Last Modified: Mon, 06 Jan 2025 15:32:18 GMT  
		Size: 822.0 KB (822014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ad534813b3adf7d6bbab7aec1fade19fd5bee8ea10f326aabaa3f7119883bb`  
		Last Modified: Mon, 06 Jan 2025 15:32:18 GMT  
		Size: 12.9 KB (12889 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; s390x

```console
$ docker pull traefik@sha256:b7e34bb766e23cf188fffc2c6201330a6b17c9348d511975f971952e4d604e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50579444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73e26f34191996e4f7f8b986f51bcb4ef1119b88b7bf4c8de24326e0f946e96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Mon, 06 Jan 2025 11:18:42 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["/bin/sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.0/traefik_v3.3.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
COPY entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 11:18:42 GMT
EXPOSE map[80/tcp:{}]
# Mon, 06 Jan 2025 11:18:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 11:18:42 GMT
CMD ["traefik"]
# Mon, 06 Jan 2025 11:18:42 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f209a02bd150e692ee81b7bc2a458ef379b501a041ea43dbd0179c735b1dd8a`  
		Last Modified: Tue, 07 Jan 2025 06:20:33 GMT  
		Size: 445.2 KB (445201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072592703c4e3052c41a983c52d0fee7f19e56b669103af3708ac44dc7ad1131`  
		Last Modified: Tue, 07 Jan 2025 06:20:34 GMT  
		Size: 46.7 MB (46674424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b30ab71bc8dfc12bf1e868ec65194cbcfe886e189832c115db1ca31ccb7c341`  
		Last Modified: Mon, 06 Jan 2025 15:28:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:7043eddffe8ba77f8fb67a2e297f01e15e3d7ef4ac90c823590c7a28c497308b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.6 KB (827579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f795d45539db0269988e41f71ccdb2a0fb628ee325a08a0187a4fc5a784e25a`

```dockerfile
```

-	Layers:
	-	`sha256:b41957ec67c23eef04234c8bf6b996b420cbf6a077e31cc1d0d16e56b6f8872d`  
		Last Modified: Tue, 07 Jan 2025 06:20:33 GMT  
		Size: 814.8 KB (814760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4489d76d054c1fde081201e63d80b6d7892bd8102ec8f53e9d49f4646b488827`  
		Last Modified: Tue, 07 Jan 2025 06:20:33 GMT  
		Size: 12.8 KB (12819 bytes)  
		MIME: application/vnd.in-toto+json
