<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.37`](#traefik21137)
-	[`traefik:2.11.37-nanoserver-ltsc2022`](#traefik21137-nanoserver-ltsc2022)
-	[`traefik:2.11.37-windowsservercore-ltsc2022`](#traefik21137-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.8`](#traefik368)
-	[`traefik:3.6.8-nanoserver-ltsc2022`](#traefik368-nanoserver-ltsc2022)
-	[`traefik:3.6.8-windowsservercore-ltsc2022`](#traefik368-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.37`](#traefikv21137)
-	[`traefik:v2.11.37-nanoserver-ltsc2022`](#traefikv21137-nanoserver-ltsc2022)
-	[`traefik:v2.11.37-windowsservercore-ltsc2022`](#traefikv21137-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.8`](#traefikv368)
-	[`traefik:v3.6.8-nanoserver-ltsc2022`](#traefikv368-nanoserver-ltsc2022)
-	[`traefik:v3.6.8-windowsservercore-ltsc2022`](#traefikv368-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.37`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:2.11.37` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.37` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.37` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.37` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.37` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.37` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.37-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11.37-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.37-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:2.11.37-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:3` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.8`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:3.6.8` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.8` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.8` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.8` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.8-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6.8-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.8-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:3.6.8-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.37`

```console
$ docker pull traefik@sha256:05ff868caaf67ef937b3228d4fe734ef8a353eab2123ac54f2a7b622d1d4b270
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

### `traefik:v2.11.37` - linux; amd64

```console
$ docker pull traefik@sha256:4674001c91bd56b9130c5ebe01f044af3caa7ca8ff7157cc5bc205d05c9587cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51146770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5dcef7c8c125ddf37fd95eb1c086d6e99820e79c1231fc095c2270d53f86a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:51 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:54 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc9526a0f604e3d338fa7c50433d35e43447dde53623ef72224d6f8898ce133`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 460.9 KB (460935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b123c779dafb0d9aebdcfdab7672246094d5816a7efb8a3fcc9c8e44a40e9`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 46.8 MB (46823646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:856fa1f768fa33dca556782b5bb4edb1c55013d78a1c2f87d62762757ee8dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bc96e74656733b3cacabbec267a36c6e8e20afe6f3198d10d9362a209647fd`

```dockerfile
```

-	Layers:
	-	`sha256:823e1e28513416fff2e9078556fdc0c2dd4d88385787a633df6d3d8f1db8cf7a`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 855.0 KB (854958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fb162df6f1dfee727effcec5664cbfcdc48bef84f2310d15c7dc79f1b98a2e`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.37` - linux; arm variant v6

```console
$ docker pull traefik@sha256:64c28f5ce85910633348d7f949b6db08053e1520432c7a3e79468d8d73d51804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46884867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c616f28cc1cef42cc47b77a19c964f48d789bebd3a82c0bc1f160bdc9514c14`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:07 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:10 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:10 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc65f8a9f6afa86222cdf70df3c7dff43da33d46cc1a5ec6520dfda2dc939928`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b83bd68d6f4f19fb27afdf75ac0a7ee6b38b849e239d5bfc8933e4578ad887`  
		Last Modified: Wed, 11 Feb 2026 18:29:19 GMT  
		Size: 42.9 MB (42853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999542a3e1881f1eaacfd9bcb3864c1f507b18061d7aeb41cab470285cdbfc47`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:b3da37a36693c97fa3222de2f3dde30ac4af2e5bf9eebaf5e98f62e0d8eb4a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5064662084552bea8433b54792270c01eb4fd8bfdc6c87684346be43d7eda46f`

```dockerfile
```

-	Layers:
	-	`sha256:53de1436faa0e4c9850add0cffad0fb81dc5e4b0252a8f627ae510f08b35d423`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 12.4 KB (12396 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.37` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5c8846e4cad0339c506ba28a7038bbea7b2bad5170d58b3be9f8973bf1004fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b639537234376e80ee76f3dbc3e3bc5ef9790b0123f0b422d60e1c76d55e70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd3bee773b2168e885eb49dad40cf36e8174e043ca1e3292c951c8813d3df0`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 463.0 KB (462997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332caafd5305deafa81b28f2240c26cde15b4346a753f546768d191ecef7f2c`  
		Last Modified: Wed, 11 Feb 2026 18:29:18 GMT  
		Size: 42.1 MB (42107629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:f416c6656271a3b24127e8c197ccd4fd756c390734621b3534af38abcaaa1d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.0 KB (867049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be44a24e171a0c206394de01279b771bee3901ca7c611f9fc3aed282f0d2557`

```dockerfile
```

-	Layers:
	-	`sha256:03be0ff48256063b98635dbcd4810e2f228617dc716d135c5d5dafb8f1500dbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 854.4 KB (854400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01e375301cebfcfe6484ffa911c2fbc73e7983acf1f3de1d00ff23bc2cab2bbc`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 12.6 KB (12649 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.37` - linux; ppc64le

```console
$ docker pull traefik@sha256:6747080deb02b751e1bbb884662dfcfad04ee656545725ab568af0dcb84e25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45352456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94331d0b80b9af11aebe59257043225a47f3bfd82727f3558b951c3bb7ee43d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbce8228c8274e447be851e758f5ab64ed430ee5e7ec09d09cf5bad455946474`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.1 MB (41058930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e062c91ce36b494688063f9ff654d3dfafe9eaa0cb74b3eb26af7505df9497f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:c104107d25219ecab051c4dcc0416d82a866f6638235c0f17d6594e4e866c9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653cbcea08145d8652c49a1f3527679b2187834b802596346fa2a0dcb2052fb`

```dockerfile
```

-	Layers:
	-	`sha256:de92697e5eb753e60165745b07ccecbdcb1b4a4c80bc1938097e3736fd2eaca5`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 854.4 KB (854359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab21386749c7e260230975a765effece9622084466c9679977cd21339863b45f`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.37` - linux; riscv64

```console
$ docker pull traefik@sha256:349398e3bb4a2fe8ed9bdfe86a9f1e6d07b341019650e06705dd44c39b12a54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b062a7ed502e7ec5dbf17cb22605fb0b0fc4ded6e76b19574b4a38fdd071ed8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:46:03 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:46:04 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:46:04 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:46:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c8945e2e9d39a884e1866b441dd2a05fb4c31aa2decdcd5d0cf3ab9c4d06`  
		Last Modified: Wed, 11 Feb 2026 18:51:11 GMT  
		Size: 45.4 MB (45425506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f3d61efbfe4b8f043f4153ee63ae9ed23317fc5c51dfe301cbf09a816182c4`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:d1f5382e8a276d5f5f043d7192343285986688230dbef090cb0d5c67ea48358f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcfb71cfe624555f7ead7ef3b453000f51b66e89198a8721cc79c0782a1254`

```dockerfile
```

-	Layers:
	-	`sha256:66d483f5e16cfa8ae3a24097503fc05aefc834d57ac35709454ff89b8981ebad`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 854.4 KB (854355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74908647b519431f28184aafdf0e754bcc93ce36a1c98b4540a1daf167390f83`  
		Last Modified: Wed, 11 Feb 2026 18:51:04 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.37` - linux; s390x

```console
$ docker pull traefik@sha256:86ac8c7f4e4d90eacbd40084fdcff8520aafdfad48b9b8e8574fcb704e9504b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49472694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db9aef2a4035db37df77311771f57fcfac6f3a94ceb4a07280ae7359169e89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:33 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a7eab13b38ec43380e27bbfc69f187fea4820fbc4366cfc6f04336d50e64fe`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 45.3 MB (45285244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf383f345ab82267ee3e1e6e74685a0c3c0fa11a3197305483d79a931d0df`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.37` - unknown; unknown

```console
$ docker pull traefik@sha256:f53e136c53bad62ebc9912451a63d32db568a211e1b0af7ba7db902790eb97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bdc226551cfbc5101a539be9cea4ffbff1fd8dcbc5f1f5c6771c5df9d88e5c`

```dockerfile
```

-	Layers:
	-	`sha256:b6c2472f791a740b943ef915d18be99ba17d3a22a12df150075a31c59873c580`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 854.3 KB (854303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2292206805b7eb2da168cf6ad8976460f66f428b02e153d97944f53cabf660`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.37-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:db761a7a7e9d0f533d1b96252a99eb9fee4adce3aaaaa44013e733e8152282c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11.37-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:e797d647dc6b3aa5688752790a728b203e94bb9b565d886b19324821d257ee9e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174279563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8f1ca5a3b8a6c4fdca2037272541ea22b4834ee5e9e48f16c461a6170e89a5`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:18:49 GMT
RUN cmd /S /C #(nop) COPY file:9478d70f16a91f8d2a000698424f9723df829454e9131d7591f95d920ce8db63 in \ 
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:18:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:18:52 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d2ca70418fbfd29a8e63036e8c18e42d592f4f5f936bfb8e985657a639fd44`  
		Last Modified: Wed, 11 Feb 2026 19:19:34 GMT  
		Size: 47.6 MB (47630605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c168cdbd9f63ce63590a5b9009bf68ac718b1a451a1703b7611f748556cf49d0`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed8df4c3b8a2175133a4912a92a40cee2463929eefd8a149a26eaa61bed458`  
		Last Modified: Wed, 11 Feb 2026 19:18:55 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad28f8c32c3452d42588788a19002a539827b464b160886f5412362f6b86e62`  
		Last Modified: Wed, 11 Feb 2026 19:18:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.37-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:692560ea78d9384d45b893228e816c6dac659b083040b9d2b3008da9f269e0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v2.11.37-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:bef93a9ef8ff2fd0eb3b6455e75b9d1e2a4f4f7e8b37d87788d2567aef2f072e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910901364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949a4b808e4ccbddf830de394d91f049586eff87df564db2df1616821f8e5f02`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:10 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.37/traefik_v2.11.37_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:11 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:12 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.37 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604deff6755e44e4586bc818a393cea8680f01c5975aaa2fb0f76639c0be754`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde1e2ec572096573af7e5e1f66a98d4adc56ce9e5c7e920c8516e0881f2bb5f`  
		Last Modified: Wed, 11 Feb 2026 18:37:44 GMT  
		Size: 48.2 MB (48238939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b710cf2bfc58d93b6bdc90a68d4b996967e7efcf64a008d9304904a919955b`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03bcd7ff08d132019228d926d2cc402532a7ecd6fd864dc2c2a947d38645cdc`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d49bdaf894fc15597e0eaf3ac36afa861974947ee5e09463cef70eeda71d2`  
		Last Modified: Wed, 11 Feb 2026 18:37:17 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:v3` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.8`

```console
$ docker pull traefik@sha256:90099f8948c828ecf0ababd711a4359a2443eba12261c1df2f548a3b1d815938
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

### `traefik:v3.6.8` - linux; amd64

```console
$ docker pull traefik@sha256:1624b11e039cd7c7f477913554ae6ccd90fb395a582fd2fd35000b8f2fb49c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52266344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de33707981b5ed4632b0e2ddccd0561d5ef981e49709b8a07da814b637f3975`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:52 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c4d5a64dd67597d77bf173daaba50d49a99f2717982dba079fa467d568454c`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 461.0 KB (460953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9db6f1c7bbc967eb6308e0572eebf6aa43f4a78dc10ac91138096e22ebd3161`  
		Last Modified: Wed, 11 Feb 2026 18:29:17 GMT  
		Size: 47.9 MB (47943201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86334337430e9b906f25f28263756e04020e6c35b06af6c2ed9c6bea384b1fe6`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:cf39b5c13e7a98e2be331625348235dda37e52f1a406d69dfa678d3bfda38f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502d7d70b4df5e8c759740ec274ba667e9ec8f7e3d6239b7802e813b1e28f3eb`

```dockerfile
```

-	Layers:
	-	`sha256:c98fc5eb7553b9457f758d94c92da012ca459afe893849e93cda55aca01f9f75`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 843.1 KB (843098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f65545e1bebadcbd30818568aa53320fdec56e3c30df52a2422671a3214705`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.8` - linux; arm variant v6

```console
$ docker pull traefik@sha256:8094eae9bf13b32e1eaa71b202508e7d8858bfcdc4853e610777ef417f925917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47564668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6e9aeb0b6e74131e9be6a47cef48c9246086352e4593370caf3ea7e3ac73e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:52 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:55 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad65e20d45ed0b7c978453eafb375a149eeab9724b0a1dce24b829a549fbe9f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 461.4 KB (461425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4068f373c2999837737de687fbc5209e28e70836da7c73076746f4d6efa370ac`  
		Last Modified: Wed, 11 Feb 2026 18:29:04 GMT  
		Size: 43.5 MB (43533054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b37a5c2cb7b3085deaf70f844443591bca19b9f146be718eb01ee41b7f4bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:4c36bf5a90e59ed1ad32ad269dd38d4eb9b17d8a5a055da14c901b03aff5f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2967be58e106f43b0639583756c1f85bae52aacc90d05f97ab71942d1ae8553b`

```dockerfile
```

-	Layers:
	-	`sha256:465ab87ebfb9f06cd0711c58c9b593f34707eac0ea43f0dc0c0159743a811c7f`  
		Last Modified: Wed, 11 Feb 2026 18:29:03 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.8` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:daf5df7f7b96cd34a1a499a275cb93c8dbc4ce58d49f98911e0583ba41cc4351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47485955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce2c8f6b868f17e0188e5d7cc8bab7db77124e6ff60df3fbebf1f4cdee94d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:28:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:28:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:28:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:28:50 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:28:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d785346774286313945e5cd584ca8ccbf47124e385df41d62ea20e2610513ab`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 463.0 KB (463032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be67ee6cbc332107abd32cd84a6c185746998935a2b543ed55d6f6f0330ccb8`  
		Last Modified: Wed, 11 Feb 2026 18:29:16 GMT  
		Size: 42.8 MB (42825463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941de6c55356c8fff9845334a9e7ddcb1fc4a333fc86742ddb4376c6946d25bb`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:c89782e40873c27c8d4df6fb41f97c53784d6fbbd863df99b170e6e4d01cca57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbde02474a605d55e4a407734a9051812961d085b512e05296738870fcd8f0cc`

```dockerfile
```

-	Layers:
	-	`sha256:8d552c5025a1e58fe69632d976c19b7a8d1621b2619befc065bf6db114ab0d29`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 842.6 KB (842552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bdeb803621be9b78e91acb6335e8e533039a290b9a588730915054e177319d6`  
		Last Modified: Wed, 11 Feb 2026 18:29:15 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.8` - linux; ppc64le

```console
$ docker pull traefik@sha256:95da16c57e031f58c06270db0c052110f6d82253a4713fedec114d011d209206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ab82fe4e440639987bda4407808765956473c04677fe1f6ca2e27a261ee7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:40 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:48 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:48 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7362847698465fa6de58e9753bbf1fb8a57c5e5f496e561c83dedde74b8ed70`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8299322f12887ec03fdf7419d03aeb32b51a51d8d1eb225a3cff430fbe47f76`  
		Last Modified: Wed, 11 Feb 2026 18:30:45 GMT  
		Size: 41.4 MB (41419472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c7d8cd6a94d986199d20a757510523022c49a96eeb83656aac2b380182b56`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:370f6e5626945ea842ba8775ad81add4e1ae4ca3b54bf84a4eb9a84e82ba7319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ebb747cb375de550f6938973f7bd23453534e43dfd3ee8663847ae2e8162ed`

```dockerfile
```

-	Layers:
	-	`sha256:a74e759d99a99ef7d93ac7834240ebfc016c0111bb0287aa0901ee07a47f05d4`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 842.5 KB (842505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082ec629956be42f77f84e1d8bb279acb7b0949860bd43403a62c5c301578fa8`  
		Last Modified: Wed, 11 Feb 2026 18:30:44 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.8` - linux; riscv64

```console
$ docker pull traefik@sha256:2d5ead50aa385ac9fdf102bf21b115f418a232ac75818b3230818568d1b7a87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50365397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e959ff03f5e018a47fb0de0230e7f0a7f5c14a1a9c20dd99b6bbc2d31abec9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:38:33 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:38:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:38:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:38:45 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:38:45 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1af5e6cc7ad430375d4f93439b88f4d2f08143e5da30be45b66332313f8dce`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 461.3 KB (461251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157ce2afdfa1828dc74f22b8e9a30b9a08f40b92d8849182767e6c49b53fbbc9`  
		Last Modified: Wed, 11 Feb 2026 18:44:28 GMT  
		Size: 46.3 MB (46318490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561558f9c4d92013e53ab11c7ab7595fd0d5115429a6a33c21814be7a6b4932a`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:9068d34e7f9a7ac7d7e3b2a26ede8dde7347b9eb3f3683735c26d1b13c5944ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ee3fce4e0bcc8a3fa4c023792513fd5300fa526e7223b434ee3ca22b67a310`

```dockerfile
```

-	Layers:
	-	`sha256:277756ba9236c2f4b6deb085fb451bf3837fea48e50ca0292a8f47d8ebdd52d3`  
		Last Modified: Wed, 11 Feb 2026 18:44:21 GMT  
		Size: 842.5 KB (842501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b584867433628f338d50c0b5ee5ec677be685cf6d6c814611bc5f1ba828033`  
		Last Modified: Wed, 11 Feb 2026 18:44:20 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.8` - linux; s390x

```console
$ docker pull traefik@sha256:5a2ad567666bf2c1c8f97aaf33d7c35d514ab04122c1c44e2642a43edf460b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50331471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce94d303d6faf90c7e84e915e508ca842da1d1a88c2b0aa66a9870ddc2c95240`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 18:29:30 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
COPY entrypoint.sh / # buildkit
# Wed, 11 Feb 2026 18:29:32 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Feb 2026 18:29:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Feb 2026 18:29:32 GMT
CMD ["traefik"]
# Wed, 11 Feb 2026 18:29:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacfa69020f22a69d26a7895ca348872f2e90dfd95f7a8d0a3d72f6efb0c2930`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 461.7 KB (461748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9247bdb02e57374b5fb9aa6a38fc8e863c5cb8dbc62051140e2c40c8c8031`  
		Last Modified: Wed, 11 Feb 2026 18:30:24 GMT  
		Size: 46.1 MB (46144022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39049e94b0c043fe013ca646e86a9cce9ab6ba51b9b998678453e106211cf57c`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.8` - unknown; unknown

```console
$ docker pull traefik@sha256:11c624059a3572625e634ddb5ce1d7458209254136cd798dca0438509dcbab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc19d4e03283097fba2a0d5cf35d144fd7225d2b3707ae65c0ebb67dc1bed6b1`

```dockerfile
```

-	Layers:
	-	`sha256:18cca3a467bbc4e7b5acaac46737e681cfd84b4b8a0f0994c6ab668395812eb6`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 842.4 KB (842447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d395ad2a9d4ecd65a750fe615be0b4a43da1a457b300d457483ef3e3e3b59d01`  
		Last Modified: Wed, 11 Feb 2026 18:30:23 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.8-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:838a02354ec87bc9f2da5d4580a9324bd63839e5fadd877dcc13703387c6d993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6.8-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:3296723e444e0a5a1dca533629d52d1c0e024ee1ca6173b3e405348af297e2c4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175379865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74feb47291a5e717c3728b37a3fc30a2b8705b86dd704afc999ef762a74ca57a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 19:16:57 GMT
RUN cmd /S /C #(nop) COPY file:060f7dbe6154711a0cb4c2f1ff4a0b4e469144f8f6f3e2ce1632a66aac2ad0e1 in \ 
# Wed, 11 Feb 2026 19:17:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 11 Feb 2026 19:17:02 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 19:17:03 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55681f2bd0eb69ddb128414715da5c37f89d935cfd73807d1cd6de7fa1d0b9a7`  
		Last Modified: Wed, 11 Feb 2026 19:17:48 GMT  
		Size: 48.7 MB (48730839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66aee8795287e3c1876569b306df08dab08be928f1b13453a5601f7745706`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaab7bbe09f17485ccb73fbcdb5106375ab7a60040d7c52b637f10770c5b95ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a238a505ccc7406b1156565a0cb3f1e8800b18ab05da73d446ad8f8cd8acf0ba`  
		Last Modified: Wed, 11 Feb 2026 19:17:08 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.8-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:v3.6.8-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8e85dc6b3205325e8ead336e9b7f7b0e4929408c8b9c9d9d2e7123967e04cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull traefik@sha256:8dc33ffe644517556d676754414cb5c30a0bd73956b725ca3a35294172b0e4e8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1912025266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12993928d606f254235acde588772ca9b86c8d1d1f6cc97ef4d58fbb29d8d50`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 18:36:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 18:37:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.8/traefik_v3.6.8_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 11 Feb 2026 18:37:19 GMT
EXPOSE 80
# Wed, 11 Feb 2026 18:37:20 GMT
ENTRYPOINT ["/traefik"]
# Wed, 11 Feb 2026 18:37:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.8 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5e36401b2fa4a668d8fd649b1fffa8794292e936a065142e888aadac1d1a1`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4611602266ffd2ee56aa83917c659a51cadd1f15b79b09de4aaee8614e32e190`  
		Last Modified: Wed, 11 Feb 2026 18:37:52 GMT  
		Size: 49.4 MB (49362800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9483ef833d3447753f2d125a95cb6043aaf8d436d46f8529f3cffee8e44959e6`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16e0601dc47c64a3d6b54a61db18eed65f8bb7c34c9556e926cbf738da56d08`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efbfcf9a88436d65dc2fb5006da1c7352b8952b566b422d6f0368acf11ee255`  
		Last Modified: Wed, 11 Feb 2026 18:37:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
