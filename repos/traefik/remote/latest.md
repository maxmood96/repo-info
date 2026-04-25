## `traefik:latest`

```console
$ docker pull traefik@sha256:4cda3393930dceff030e144b46260e96e1337c9cfaa4fed81c90cb8f4d498f57
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
$ docker pull traefik@sha256:e08f2a770aee6b838b4c1be5fe25569a653b1592e4673a240414bc8bc4ad0aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53059957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b891d7b6239bcf027f75824a5310763ea62e2bf75c2478a9b35ca31e76cbebaf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:38:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:38:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:38:08 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:38:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:38:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:38:08 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:38:08 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5680a1772d7dc19d390e0cd1994c8511daa8871fcaf05b7c155512830e4262dc`  
		Last Modified: Wed, 22 Apr 2026 17:38:30 GMT  
		Size: 455.7 KB (455663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332492583edbf3ab346f172a9dc93586b3998eec2fde0034cabc37b047c283d6`  
		Last Modified: Wed, 22 Apr 2026 17:38:32 GMT  
		Size: 48.7 MB (48739735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e03085f8847d6bf2c937cc94cc92d70c6579500952dfe5a0ec70ba11164138`  
		Last Modified: Wed, 22 Apr 2026 17:38:30 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a12c36408a7bd505fc2ff992a8a5648d41394bdfd25db8ae733d9643c5581afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **861.2 KB (861235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb83aabe9f8c021825a2a6cda592abe5fc6162b17eef8c6e2fb4b29cdb63652`

```dockerfile
```

-	Layers:
	-	`sha256:ed3cae88705a700f055551d1554f10de187c444a31c5f0fb84729ec046a2bb67`  
		Last Modified: Wed, 22 Apr 2026 17:38:30 GMT  
		Size: 848.3 KB (848344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daae0b6e2271b862d919fc0967bd6d91f86f8822296591545f47eeae5a9346b5`  
		Last Modified: Wed, 22 Apr 2026 17:38:30 GMT  
		Size: 12.9 KB (12891 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f90f0ac7d9b8501ef87e38e5659aae267a74e595c47da06dea714eff61f1e5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48303714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a96925048642a6351802be3555ea0917e5845e8986f558b612d517243fe7b28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:32 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:35 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22733e9b782bed0a545f8955760b4174c55fa47aa4d8e54388e03494e2d1eac9`  
		Last Modified: Wed, 22 Apr 2026 17:37:43 GMT  
		Size: 456.5 KB (456522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d473f6af8b7efa2f7a61c443d2fadf8452ba4889c0754304bab40133236a44`  
		Last Modified: Wed, 22 Apr 2026 17:37:45 GMT  
		Size: 44.3 MB (44274961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9dd42d46bd53c4318ba390327ec9dc73c988dd3ee12dea02362f8447e6cccd`  
		Last Modified: Wed, 22 Apr 2026 17:37:44 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:20569a6b46da407b873c9d8bfef76653d47f72c96d730fd85b187b61d908ae94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf9f6ba443cb3de6aee3ba8d24cf8ae9561cb558f51ef024d2ce7de0d10eef7`

```dockerfile
```

-	Layers:
	-	`sha256:1dbb2266182bc5c586c904aaf5ba12b4fdb47426ffc237bef36890a701837320`  
		Last Modified: Wed, 22 Apr 2026 17:37:44 GMT  
		Size: 12.8 KB (12801 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4c1bdb3fba3af27989d8cd02f657e60b9839b121f1e9117f60737a6341115493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48215599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7212fe3335b5e2ac127f372dda647ae481f02659cfe01c1ab721770c36ce44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 17:37:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:37:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:37:46 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:37:46 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:37:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:37:46 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:37:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e166ec0e4674661a410b67635772553a4f58d138af8cecd9adce5f2a0324b2`  
		Last Modified: Wed, 22 Apr 2026 17:38:11 GMT  
		Size: 457.9 KB (457923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07db3021e49c2811a21c29f69c3826e2fc79555aa8f26f53c592eac0715f29a2`  
		Last Modified: Wed, 22 Apr 2026 17:38:12 GMT  
		Size: 43.6 MB (43557437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31003a85f1dac10211707c9649f4d93bf0b8ecfbb2394766d81d192da3eb5424`  
		Last Modified: Wed, 22 Apr 2026 17:38:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:cbe1db4bebd4aa1f9cb90f5875cd11ced96f3db94554ba84f8f51ba438c271bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.9 KB (860856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b3220be206bbcc928800bedb78fa7303e0ab0765e5e451ea5fd5d26483154f`

```dockerfile
```

-	Layers:
	-	`sha256:2f05f249eba565579619c446ce16cb0a1d48824c4162908e2875f5672b0d1534`  
		Last Modified: Wed, 22 Apr 2026 17:38:11 GMT  
		Size: 847.8 KB (847798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8bb57b511ebace3eb47d27f2ed2a2abdc9bb0829cf24ed33a3393b03087ba0`  
		Last Modified: Wed, 22 Apr 2026 17:38:11 GMT  
		Size: 13.1 KB (13058 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:d3448c4e3736032fd827c32be97a9ecc31ed45b0b75603c0e2a6d0b5394e656d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46435755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482e299a6fd2d5d33eb48b2bad31e2346e2036d04298d95cf9e7c531ddb24e29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:08:00 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 20:18:58 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 20:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 20:18:58 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 20:18:58 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce53e29a62df07c200ac0d7cc718585a7031556056c94626ccbb010496ad7d`  
		Last Modified: Wed, 15 Apr 2026 21:08:51 GMT  
		Size: 458.3 KB (458325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b774a30a12f405bcb7979b954f7fd8c2ff8a54ccc2d617bfbcbe6455ba17fda2`  
		Last Modified: Wed, 22 Apr 2026 20:19:58 GMT  
		Size: 42.1 MB (42146132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b644e6a105ab0991360d4428c9d9641fea18e2875faa4eb2ccf2f84b7bea29b`  
		Last Modified: Wed, 22 Apr 2026 20:19:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:e78d935d2e8160c88e327f415783933038c84ea2526e43f5d7eb4d1fbf486898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.7 KB (860711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f9a698a2e58d65750221e770981fc01be438059b4ca29463f69cd69886e82`

```dockerfile
```

-	Layers:
	-	`sha256:f1c243212b90b7f0aec5f362b451356d41d27657acb3ef34964f6e60b16abfd5`  
		Last Modified: Wed, 22 Apr 2026 20:19:56 GMT  
		Size: 847.8 KB (847751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f33d00107fa774a3f3f7005cb1382e412c64084e2cf59f5dd1045754ae1c433`  
		Last Modified: Wed, 22 Apr 2026 20:19:56 GMT  
		Size: 13.0 KB (12960 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:1759c5c29c6fdbe4143acb887187e521f305fed74c3cb7727218b17858f6379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51121707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1290b6f1c6ba191008f69223efb2705839cbb603fc92d2c1df2334de3d3eab76`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Sat, 25 Apr 2026 18:28:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Sat, 25 Apr 2026 18:35:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Sat, 25 Apr 2026 18:35:17 GMT
COPY entrypoint.sh / # buildkit
# Sat, 25 Apr 2026 18:35:17 GMT
EXPOSE map[80/tcp:{}]
# Sat, 25 Apr 2026 18:35:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 25 Apr 2026 18:35:17 GMT
CMD ["traefik"]
# Sat, 25 Apr 2026 18:35:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa86f96704c7abcae65c8930cd34ae1dbc4acb6727e475216f605e390365e73`  
		Last Modified: Sat, 25 Apr 2026 18:34:29 GMT  
		Size: 456.0 KB (456001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab5ce061f77c8cac979832d06ae888ba51870dff3bd04fd3375f0024bf8d014`  
		Last Modified: Sat, 25 Apr 2026 18:40:35 GMT  
		Size: 47.1 MB (47077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d24bc606a9e65f8aa46d12bc091cbfced40e0b5ae05e32f99b359df613ba118`  
		Last Modified: Sat, 25 Apr 2026 18:40:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:1d7ee06ad2e250ddf3582c62b31eee69c4ba0ab5b3d0959389057d73207aae13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.7 KB (860708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66cea57b5ad1717b46ed95e979b8aa639753411ac1e0fccc443a40d56330d6e`

```dockerfile
```

-	Layers:
	-	`sha256:fc714a2abc05342d9ec6a84faa81fac2e7cff784d89eb4be9d4b4f7a7f1b8859`  
		Last Modified: Sat, 25 Apr 2026 18:40:27 GMT  
		Size: 847.7 KB (847747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1382bb9e71afd51bf1149f3ba0e0019c5065c41706c8429ac58e88510da6238e`  
		Last Modified: Sat, 25 Apr 2026 18:40:27 GMT  
		Size: 13.0 KB (12961 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:90f5edf8fa223e640b210d48db1a5e3eb103576c6c5219bfcaf246f819377c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51104876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401afc8ca2c418af4499293d4be9a2a6cbf193c7e790a968e2ce62fc3a2992d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.14/traefik_v3.6.14_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 17:36:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 17:36:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 17:36:13 GMT
CMD ["traefik"]
# Wed, 22 Apr 2026 17:36:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.14 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935dd66668d2f6e060f9d991a73aee8127a53466085251bae64e750e36112cdc`  
		Last Modified: Wed, 15 Apr 2026 20:42:42 GMT  
		Size: 456.7 KB (456660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d438ff2bdb8765ae8719e5f6488f92216422e177c1e6e3855161c69c78aae9`  
		Last Modified: Wed, 22 Apr 2026 17:37:12 GMT  
		Size: 46.9 MB (46921315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a04b89a9e7cd55cf340917745b573248f7da1e1c5ce448daea4c3c6fa28d2b9`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:763f23c0dcc86968cf00a7ae031ea0e6157d1ffed4598d75dee96091418b777c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **860.6 KB (860581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27670c00335b63ef2c59f85a31c3767e59ce0045e331578734a465e884c7074c`

```dockerfile
```

-	Layers:
	-	`sha256:acc0113b399a19904cf7aa4d71bd16a2e04a70c6c05ec5e9c283d7634438b228`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 847.7 KB (847691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3061f99b7cf3a9b2ee4c8c7120a5ccf3ff8cd54d2c2244eedc627594d00c00ab`  
		Last Modified: Wed, 22 Apr 2026 17:37:11 GMT  
		Size: 12.9 KB (12890 bytes)  
		MIME: application/vnd.in-toto+json
