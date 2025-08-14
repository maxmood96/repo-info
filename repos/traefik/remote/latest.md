## `traefik:latest`

```console
$ docker pull traefik@sha256:4e7175cfe19be83c6b928cae49dde2f2788fb307189a4dc9550b67acf30c11a5
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

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:4217388f0a14adfe5f57f7b7bd4e3462fbfbb07d60d034c578bc622b7a75e715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58270434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc59587f6a8eac05a205bb5b3b6008d0b5ecdd7b2b3769f2215bcdb7149add`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a77cce7b9030ef43c8992839f7db9cb47d63e1c749c21e97bd0943f46c6e2`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012960e13f62cf708b5ba6d24574d0661185b3e57fd42494b5794afa8274738f`  
		Last Modified: Wed, 23 Jul 2025 16:33:26 GMT  
		Size: 54.0 MB (54022632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183886becb4e0ba33c84d6b07fd82daa1f7d6bdc83343e04679299d953b850eb`  
		Last Modified: Wed, 23 Jul 2025 16:33:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:8e2f62bae91ddcc864f32870b7078e41e28d90d0a4291de34f564cedc557beab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.1 KB (837125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a734e03da0a5a710c40c81bd790faf53b534b0719525730090b7291da724524b`

```dockerfile
```

-	Layers:
	-	`sha256:282527a0a03cfd737e02bf3623224f46faeeeefeccebbf1b17698473ef3ac149`  
		Last Modified: Wed, 23 Jul 2025 18:10:02 GMT  
		Size: 824.3 KB (824314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bccfa3e8f4c10987a783a7fbff303a5e8b3731a08b9f71477dbb862cd08b1c`  
		Last Modified: Wed, 23 Jul 2025 18:10:03 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0b0dbea70c439fa5c5a5480077004c0f911ba65b1209ca1a149ba2b965d111b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53384210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e56750485290d031731e52cf8fe6012720ef4eda8cfb28d927560ff5c507fe4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6440988a44fe9fbb48d7ac4834b1999a9e5936dc068dd9f6ac759ce205034619`  
		Last Modified: Wed, 23 Jul 2025 16:32:41 GMT  
		Size: 49.4 MB (49434649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1efcee92600fed1d70a62da821758b21950fa90112705046f2fdfcbffa5553c`  
		Last Modified: Wed, 23 Jul 2025 16:32:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a6c1c2af7ba745b9b60f54695998d73ffb1d1bf2fcf5f49cafa93c5ed4b30e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09cc67fa17c0321afb5e0a73b8709e5e889a1c62ce84641b3b58339306c1511`

```dockerfile
```

-	Layers:
	-	`sha256:2bc68775e310c47c38a508767be7f307613eb56f1715f2a63bc60571cbf44697`  
		Last Modified: Wed, 23 Jul 2025 18:10:06 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:3e93bb0c75ca146b0521503d17112aad800894b0f66c1050331d41e13bc17e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54105546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9a0557749b62d85930d70ed0d27e50ce3a41a0a6227affdd92e86a3af4f28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49647356458ff913b73227527c44d6be67dd593b69027f6802869b3d59f60464`  
		Last Modified: Wed, 23 Jul 2025 19:30:27 GMT  
		Size: 449.6 KB (449554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407709d0553da37534302999ad3d63a22ce776c5f50062bb21722aaa71166ae4`  
		Last Modified: Wed, 23 Jul 2025 19:30:16 GMT  
		Size: 49.5 MB (49524874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6438107ea0722796b9adf9c0c2ae48badf4b1a72f0fcfe0a306e2e6b769bbc5d`  
		Last Modified: Wed, 23 Jul 2025 19:30:12 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:07167916507caaf43894bc3daffa0a9b8570272e9f8ea3a96b3624d10206eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d98f8246b44d3477a654fce67d22de4a00cd16da691168d025f3a11fe49b3a5`

```dockerfile
```

-	Layers:
	-	`sha256:82a90cc95a1995aff060f9ecd661f10f476dd23f0c641c5fa41b67b6fc133924`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 824.4 KB (824418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2679e6196ab944225611475f1f5a5e2542fe6ee1a274a02cb392d9d2c353a8`  
		Last Modified: Wed, 23 Jul 2025 21:09:38 GMT  
		Size: 13.0 KB (12977 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:93286464e0ca672a2ea18bb3efa5f60ddd23768f686174e2939fbfaa144bfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51483174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b43e2f6dea603d51be26928e56a5178098fadc5d0f07c88bc60a94a66c07c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624dfbf95e383e8d6e12920f348c25b17b22bf30df4635c79abaef9e8c1794b`  
		Last Modified: Tue, 15 Jul 2025 22:39:58 GMT  
		Size: 450.0 KB (449975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191e2811077a5d748ecc713d8f518afd15e160941c7badfee222c1c9b5886bb`  
		Last Modified: Wed, 23 Jul 2025 16:34:12 GMT  
		Size: 47.3 MB (47305720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d72bc0e076684dc5ed986dfa0d2ca855e1077bbe0f1583374298aafeafa780`  
		Last Modified: Wed, 23 Jul 2025 16:34:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6a57a10dfba223cfff09d028085fa0a642814c82f808d74075332708ca17fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a6c1184bbf49c846487295f6b74826c02a478443c59841fedb3d91aaca13bf`

```dockerfile
```

-	Layers:
	-	`sha256:bb8cb8e02cca96ef065ac0ea0285002d48caab12761e632b668552fc9b5742f3`  
		Last Modified: Wed, 23 Jul 2025 18:10:11 GMT  
		Size: 822.4 KB (822421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ad4929c8f9dfc8efa3f203fde45a5899b0d5d4e88b7004f023c40b080a56b4`  
		Last Modified: Wed, 23 Jul 2025 18:10:12 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:7dfd722efffe8121f0b277c0d9c2ce8e4d9541495a9421a9f456497d15218275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56237881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb4df812d41071c13e9f479a459ad26cc520100c1029b512d6c5cc70f83a63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa12c4e8b7e986532d6ad4028e8c7222143805af000d470927fd24ff5e2c1c61`  
		Last Modified: Tue, 15 Jul 2025 22:47:42 GMT  
		Size: 448.6 KB (448587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a274f9d4f1aac15201205bf6fe750f485b491b4b3c74a21cd763932a81257766`  
		Last Modified: Wed, 23 Jul 2025 16:35:16 GMT  
		Size: 52.1 MB (52143954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47c2b991d95bb77342a8233028abf9649b48c9ef0d555e5104265de66083a5`  
		Last Modified: Wed, 23 Jul 2025 16:35:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:ccb9b8c41ff6888e33d2cff3acfe24fede45c239c1a308f6cd8b002fbed711dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 KB (835174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9986a3203b5eedb08bcda7a913a4ef1001d3e50e2fa25d6eaa4617d374d69cf`

```dockerfile
```

-	Layers:
	-	`sha256:d92b365a6075562ba85ba9d171482df5c86be64820427341d498395d2efd1693`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 822.4 KB (822363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d223b530245f532286c20a5d3bc9f63a8591f2954fd307f0a493e327f85303`  
		Last Modified: Wed, 23 Jul 2025 18:10:18 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json
